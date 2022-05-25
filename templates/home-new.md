export const meta = {
  name: "Home New",
}

export const Template = ({ filename, meta, children }) => {
  return (
    <div className="p-8 sm:p-16 mx-auto max-w-full w-full antialiased prose text-black pt-10">
      <div className="grid md:grid-cols-3 gap-8 mt-20">{children}</div>
    </div>
  )
}

export default (props) => <Template {...props} />

{/* Sample data */}

# Plain template

Some sample text.
