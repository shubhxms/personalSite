export const meta = {
  name: "Drafts",
}

export const Template = ({ filename, meta, children }) => {
  return (
    <div className="p-8 sm:p-16 mx-auto max-w-full w-full antialiased prose text-black pt-10 font-serif">
      <h1 className="text-center mb-20">My favorite things</h1>
      <div className="w-full bg-white px-12 py-6 rounded-md shadow-lg">{children}</div>
    </div>
  )
}

export default (props) => <Template {...props} />

{/* Sample data */}

# Plain template

Some sample text.
