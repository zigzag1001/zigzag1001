<p align="center">
<b>Hi there 👋</b>

<p align="center">
<img loading="lazy" src="new/p1p2_concat.gif">

PixelWind

`./main.exe ".\smallerbannerCopy - Copy.png" pxlBleed 17 4 17`
<details>
  <summary>p1</summary>
  <img loading="lazy" src="new/p1.gif">
</details>

`./main.exe ".\smallerbannerCopy.png" pxlBleed 17 4 17`
<details>
  <summary>p2</summary>
  <img loading="lazy" src="new/p2.gif">
</details>

`./main.exe ".\smallerbannerCopy - Copy.png" pxlWind 7 2 20`
<details>
  <summary>still</summary>
  <img loading="lazy" src="new/still.gif">
</details>

FFmpeg

`ffmpeg -i p2.gif -filter_complex "hflip" p2_flip.gif`
<details>
  <summary>flip p2</summary>
  <img loading="lazy" src="new/p2_flip.gif">
</details>

`ffmpeg -i p1.gif -filter_complex "reverse" p1_rev.gif`
<details>
  <summary>reverse p1</summary>
  <img loading="lazy" src="new/p1_rev.gif">
</details>

`ffmpeg -i p2_flip.gif -filter_complex "reverse" p2_flip_rev.gif`
<details>
  <summary>reverse p2</summary>
  <img loading="lazy" src="new/p2_flip_rev.gif">
</details>

`ffmpeg -i p1.gif -i p1_rev.gif -filter_complex '[0:0] [1:0] concat=n=2:v=1[v]' -map '[v]' p1_concat.gif`
<details>
  <summary>boomerang p1</summary>
  <img loading="lazy" src="new/p1_concat.gif">
</details>

`ffmpeg -i p2_flip.gif -i p2_flip_rev.gif -filter_complex '[0:0] [1:0] concat=n=2:v=1[v]' -map '[v]' p2_concat.gif`
<details>
  <summary>boomerang p2</summary>
  <img loading="lazy" src="new/p2_concat.gif">
</details>

`ffmpeg -i p1_concat.gif -i still.gif -filter_complex '[0:0] [1:0] concat=n=2:v=1[v]' -map '[v]' p1still_concat.gif`
<details>
  <summary>add pause</summary>
  <img loading="lazy" src="new/p1still_concat.gif">
</details>

`ffmpeg -i p1still_concat.gif -i p2_concat.gif -filter_complex '[0:0] [1:0] concat=n=2:v=1[v]' -map '[v]' p1p2_concat.gif`
<details>
  <summary>combine</summary>
  <img loading="lazy" src="new/p1p2_concat.gif">
</details>

<!--
**zigzag1001/zigzag1001** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
