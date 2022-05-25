export const QuiltGrid = (props) => (<div>
  <SectionHeading href="/quilts">Art Quilts →</SectionHeading>
  <div className="grid gap-y-2">
    <QuiltPreview v="v1608647486" id="vgv0zvmskkib6gsnhbtg" artist="cezanne" />
    <QuiltPreview v="v1608647502" id="r0euebpuahx2qh28ovfk" artist="monet" />
    <QuiltPreview v="v1608647513" id="zw1ztlsq66sm8st3l8no" artist="schiele" />
  </div>
</div>)

export const QuiltPreview = (props) => (
  <a href="/quilts" aria-label="quilt">
    <div
      className="bg-gray-100 bg-cover bg-center hover:opacity-75 transition duration-300 ease-in-out"
      style={{
        width: "100%",
        height: 0,
        paddingBottom: "calc(33% - 0.25rem)",
        backgroundImage:
          "url(https://res.cloudinary.com/djp21wtxm/image/upload/" +
          props.v +
          "/" +
          props.id +
          ".png)",
      }}
    ></div>
  </a>
)

export const Artworks = () => {
  return (
    <>
      <div className="grid grid-cols-2 sm:grid-cols-3 gap-2">
        {artworks.map((artwork, index) => (
          <ArtworkPreview
            v={artwork.thumbV}
            id={artwork.thumbId}
            title={artwork.title}
          />
        ))}
      </div>
    </>
  )
}

export const ArtworkPreview = (props) => (
  <div>
    <img
      alt={props.title}
      className="w-full hover:opacity-75 transition duration-300 ease-in-out my-0"
      src={
        "https://res.cloudinary.com/djp21wtxm/image/upload/" +
        props.v +
        "/" +
        props.id +
        ".png"
      }
    />
  </div>
)

export const SectionHeading = (props) => {
  const className =
    "inline-block font-bold text-black text-xl rounded-md mt-2 mb-2 py-[3px]" +
    (props.href
      ? " hover:bg-gray-100 -ml-1 px-1 transition duration-200 ease-in-out"
      : "")
  const heading = <h2 className={className}>{props.children}</h2>
  if (!!props.href) {
    return <a href={props.href}>{heading}</a>
  } else {
    return heading
  }
}

export const ProjectPreview = (props) => {
  const extras = props.a ? { target: "_blank" } : {}
  const mb = props.compact ? "mb-3" : "mb-6"
  const className =
    "no-underline !important hover:no-underline font-semibold text-black rounded-md hover:bg-gray-100 -ml-1 p-1 transition duration-200 ease-in-out"
  let titleEl
  if (props.a) {
    titleEl = (
      <a className="hover:no-underline" href={props.href} target="_blank">
        <span className={className}>{props.name}</span>
      </a>
    )
  } else {
    titleEl = (
      <a className="hover:no-underline" href={props.href}>
        <span className={className}>{props.name}</span>
      </a>
    )
  }
  return (
    <div className={mb}>
      {titleEl}
      <div className="-mt-4">{props.children}</div>
    </div>
  )
}

export const Arrow = (props) => {
  return (
    <div
      className="block bg-black bg-opacity-50 hover:bg-opacity-75 rounded-full w-16 h-16 border-2 border-white border-opacity-75 cursor-pointer transition duration-300 ease-in-out flex items-center justify-center"
      onClick={props.onClick}
    >
      <img
        className={"w-6 h-6" + (props.left && " transform rotate-180")}
        src="https://res.cloudinary.com/djp21wtxm/image/upload/v1608998684/y6v6hyes7ncoakzthhfj.svg"
      />
    </div>
  )
}
