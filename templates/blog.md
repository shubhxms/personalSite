export const meta = {
  name: "Blog"
}

export const Template = ({ filename, meta, children }) => {
  return <div className="p-8 sm:p-16 mx-auto max-w-screen-md w-full antialiased prose text-black">
    {children}
  </div>
}

export default (props) => <Template {...props} />

{/* Sample data */}

# Plain template

Some sample text.