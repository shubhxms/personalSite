---
title: Shubham Shah
---
import { LightningBoltFill } from "https://cdn.motif.land/motifheroicons@0.0.10"
import { NavigationBar } from "https://cdn.motif.land/motifmenus@0.0.18"

<NavigationBar items={[
    { title: "Docs", href: "/docs" },
    { title: "About", href: "/about" },
    { title: "Blog", href: "/writings" },
    { Icon: "UilGithub", href: "https://github.com/motifland/yfs", className: "w-5 h-5 sm:w-6 sm:h-6 text-slate-800" },
  ]}
  buttonTitle="Sign In"
  buttonHref="/login"
  Icon={<LightningBoltFill className="w-6 h-6 text-amber-500"/>}
/>
<div style={{ height: 40, margin:!400, marginTop:!0 }} />

<div className="grid lg:grid-cols-1">
<div>
<p className="font-medium text-3xl">
  sup, <b>shubham</b> here!
</p>
  <p className="font-medium" style={{font:"karla"}}>**computing × tinkering**</p>

<p className="mt-3" />

I am a **shadowy super coder**, **open-source connoisseur**, **internet native** and a **wannabe polymath**. I am also a honorary member of the **Scouts Regiment** (*shinzo wo sasageyo*).
<br/>In my free time I am mostly **computing** or **tinkering** with stuff or **reading** something.
<br/>I am interested in **scripting**, **web-developement**, **decentralization**, **crypto(graphy, currency)**, & **STEAM**


</div>
</div>

<div style={{ height: 12 }} />

{/* ==================================== */}
{/* Art ================================ */}
{/* ==================================== */}

<div className="grid md:grid-cols-2">
  

{/* Writings ========================= */}

{' '}

<div>
  <SectionHeading>Writings</SectionHeading>
  <ProjectPreview
    href="/8pen"
    name="Is there a natural way to write on small devices?"
  >
    Whenever we have an idea or a random thought, we reach out for pen and
    paper. This is often the fastest and easiest way to take a note. We enjoy
    handwriting because it is natural. So one may ask: *is there a natural way
    to write on small digital devices?*
  </ProjectPreview>
  <ProjectPreview
    href="https://res.cloudinary.com/djp21wtxm/raw/upload/v1608722144/zdefsd1mzk4fzjftpqgf.pdf"
    name="Ramification Theory"
    a
  >
    My Part III essay at Cambridge, where I present a theorem of Tate which
    relates *p*-adic representations with a "Hodge-Tate decomposition" to
    "locally algebraic" ones.
  </ProjectPreview>
  <ProjectPreview
    href="https://res.cloudinary.com/djp21wtxm/raw/upload/v1608722285/tl4mr3fobk5bgzz5890q.pdf"
    name="Higher Norm Fields"
    a
  >
    A short note on the connection between Scholl's strictly deeply ramified
    towers and Fontaine-Wintenberger's arithmetically profinite extensions, in
    the general case of local fields with imperfect residue fields, using the
    ramification filtration of Abbès and Saito.
  </ProjectPreview>
</div>
<div>
  <SectionHeading>Projects</SectionHeading>
  <ProjectPreview
    href="https://www.youtube.com/watch?v=q3OuCR0EpGo"
    name="8pen"
    a
  >
    A fast and natural input method for touch devices.
  </ProjectPreview>
  <ProjectPreview
    href="https://github.com/michaelfester/artquilts"
    name="Artquilts"
    a
  >
    Create quilts of your favorite artists.
  </ProjectPreview>
  <ProjectPreview
    href="https://github.com/michaelfester/mastodon"
    name="Mastodon"
    a
  >
    A next-word prediction engine for Python and C++.
  </ProjectPreview>
  <ProjectPreview
    href="https://github.com/michaelfester/doodle"
    name="Doodle"
    a
  >
    Generate natural 8pen doodles.
  </ProjectPreview>
  <ProjectPreview
    href="https://chrome.google.com/webstore/detail/keyboard-shortcuts-to-clo/dkoadhojigekhckndaehenfbhcgfeepl"
    name="Tabasco"
    a
  >
    Chrome extension adding keyboard shortcuts to close tabs.
  </ProjectPreview>
  <ProjectPreview href="/air" name="Air">
    Concept video for a mesh network of AI assistants. With <a
      href="https://www.dokraphael.com"
      className="hover:underline"
      target="_blank"
      rel="noreferrer">Dok</a>.
  </ProjectPreview>
</div>
</div>

{/* ==================================== */}
{/* Projects =========================== */}
{/* ==================================== */}



<p className="py-8 mt-[100px]" />

Built with <a className="underline" href="https://motif.land" target="_blank">Motif </a>

<div className="h-[50px]" />

{/* ==================================== */}
{/* Definitions ======================== */}
{/* ==================================== */}




export const SectionHeading = (props) => {
  const className =
    "inline-block font-bold text-black text-xl rounded-md mt-2 mb-2 py-[3px] hover:bg-gray-100 -ml-1 px-1 transition duration-200 ease-in-out"
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
