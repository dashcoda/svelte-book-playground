<script>
  // import { onMount } from "svelte";
  // import { onDestroy } from "svelte";
  // import { beforeUpdate, afterUpdate } from "svelte";
  import { tick } from "svelte";

  // onMount

  // onMount(() => {
  //   const canvas = document.getElementById("canvas");
  //   // @ts-ignore
  //   const ctx = canvas.getContext("2d");
  //   ctx.fillStyle = "#ddd";
  //   ctx.fillRect(0, 0, 100, 100);
  //   ctx.fillRect(100, 100, 200, 200);
  // });

  // onDestroy

  // let now = new Date();

  // const timer = setInterval(() => {
  //   now = new Date();
  // }, 1000);

  // onDestroy(() => {
  //   clearInterval(timer);
  // });

  // beforeUpdate/afterUpdate

  // ['投稿0', '投稿1', ..., '投稿99']の配列を生成
  // let contents = Array.from({ length: 100 }, (_, i) => `投稿${i}`);

  // function handleClick() {
  // タイムラインの先頭に項目を追加
  //   contents = [
  //     ...Array.from({ length: 100 }, (_, i) => `投稿${i - 100}`),
  //     ...contents,
  //   ];
  // }

  // let prevHeight;

  // beforeUpdate(() => {
  //   const element = document.getElementById("timeline");

  //   if (element) {
  //     prevHeight = element.scrollHeight;
  //   }
  // });

  // afterUpdate(() => {
  //   if (prevHeight) {
  //     const element = document.getElementById("timeline");
  //     const diff = element.scrollHeight - prevHeight;
  //     element.scrollTop += diff;
  //   }
  // });

  // tick

  let clicked = false;

  async function handleClick() {
    // 状態を変更
    clicked = true;
    // 状態の更新が反映されるまで待つ
    await tick();

    const canvas = document.getElementById("canvas");

    // @ts-ignore
    const ctx = canvas.getContext("2d");
    ctx.fillStyle = "ddd";
    ctx.fillRect(0, 0, 100, 100);
    ctx.fillRect(100, 100, 200, 200);
  }
</script>

<!-- onMount -->
<!-- <canvas id="canvas" width="200" height="200" /> -->

<!-- onDestroy -->
<!-- <div>現在の時刻は{now.toLocaleString()}です。</div> -->

<!-- beforeUpdate/afterUpdate -->
<!-- <div id="timeline">
  {#each contents as item}
    <div>{item}</div>
  {/each}

  <button on:click={handleClick}> タイムラインを更新 </button>
</div> -->

<div>
  <button on:click={handleClick()}>表示</button>
</div>

{#if clicked}
  <canvas id="canvas" width="200" height="200" />
{/if}

<style>
  /* #timeline {
    width: 300px;
    height: 300px;
    border: 1px solid gray;
    overflow: auto;
  } */
</style>
