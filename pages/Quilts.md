---
meta:
  og:title: Quilts - Michael Fester
  og:image: "https://res.cloudinary.com/djp21wtxm/image/upload/c_limit,w_800/v1608647502/r0euebpuahx2qh28ovfk.png"
class:
  body: bg-black
  container: bg-black max-w-lg mx-auto
  a: transition duration-300 ease-in-out
---

<a className="absolute left-6 top-6 sm:left-12 sm:top-12" href="/"><Logo /></a>

<div className="h-[80px]" />

<QuiltPreview v="v1608647486" id="vgv0zvmskkib6gsnhbtg" artist="Paul Cézanne" />
<QuiltPreview v="v1608647502" id="r0euebpuahx2qh28ovfk" artist="Claude Monet" />
<QuiltPreview v="v1608647513" id="zw1ztlsq66sm8st3l8no" artist="Egon Schiele" />

<div className="h-[120px]" />

{/* Definitions */}

export const QuiltPreview = (props) => <><div class="text-yellow-100 text-xs font-medium mt-8 mb-2 opacity-75">{props.artist}</div>
  <div class="bg-gray-100 bg-cover bg-center" style={{
  width: "100%",
  height: 0,
  paddingBottom: "calc(33% - 0.25rem)", backgroundImage: "url(https://res.cloudinary.com/djp21wtxm/image/upload/" + props.v + "/" + props.id + ".png)"}}>
  </div></>

export const Logo = () => <svg class="fill-current text-yellow-100 hover:opacity-75 transition duration-300 ease-in-out" width="32" height="32" viewBox="0 0 77 77" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M23.5892 32.0047C17.0685 30.4613 13.2974 17.3242 5.62954 23.3048C-5.6552 32.1064 23.0952 37.9223 22.0814 43.5429C21.5045 46.7412 19.0835 45.71 13.4844 46.6677C7.88529 47.6255 9.18846 56.958 12.5833 58.1931C15.9781 59.4281 25.7367 48.4964 30.9384 48.4964C36.14 48.4964 34.3682 58.0087 38.7653 65.4283C42.2197 71.2573 49.8769 73.5951 53.9925 67.9466C59.5714 60.2896 33.0646 43.334 38.7616 36.2153C43.1928 30.6783 52.8824 47.6406 60.2878 54.9338C67.6932 62.2269 80.1422 48.587 71.652 38.3993C63.1618 28.2115 46.8992 40.5461 47.0971 32.9575C47.295 25.369 75.5767 21.07 61.6987 9.74735C52.8119 2.49688 44.4494 29.9087 39.5491 28.38C34.6488 26.8512 49.1252 11.5986 36.14 6.25036C27.1014 2.52761 25.4065 7.31447 29.1412 17.9915C32.8759 28.6685 30.1099 33.548 23.5892 32.0047Z" />
</svg>
