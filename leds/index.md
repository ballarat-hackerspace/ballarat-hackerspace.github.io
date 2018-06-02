---
layout: default
title: Control our LED strip
---
<center>
<input style="font-size:200%; margin:1em;" type='text' onkeydown="if(event.key === 'Enter') { changeString(this.value, this); }"><br>Type some text and press 'enter'
</center>

<script>
function changeString(t, e) {
  $.ajax({
    url: "https://ballarathackerspace.org.au/ws2812/"+t,
    success: function(r) {
      console.log(r);
    }
  });
  e.value="";
}
</script>
