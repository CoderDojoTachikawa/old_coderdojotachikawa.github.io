<template>
  <div class='flex items-center min-h-300'>

    <!-- メンバー紹介サイトを組み込みます -->
    <div class="w-screen bg-white">
      <iframe style="height: 44rem;" src="https://member-cd.web.app/?dojo=tachikawa" width="99%" id="member-frame" frameborder="0" scrolling="yes" allowfullscreen></iframe>
    </div>

  </div>
</template>

<script>
  // 高さを自動調整します
  window.addEventListener('message', function(e) {
    if(e.origin=="https://member-cd.web.app"){
      document.getElementById('member-frame').height = e.data + 120;
    }
  }, false);
</script>