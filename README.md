# help2start
### Here I'll collect solutions for minor problems, code for tricky tasks and some other stuff.

*README.md -> what is .md? .md are files formatted in MarkDown language. Markdown is a markup language that you can use to add formatting elements to plaintext text documents. Here more [info](https://www.markdownguide.org/getting-started/). How can I format text in .md? Here some [syntax](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax).*

#### Examples: (use a '#' in front of the text for the biggest text, '##' for smaller and so on)
- **this text is bold** (put your text between '**')
- *italic text* (use simple '*')
- > 'quote me' (use a '> ')
- show some code like `npm init` (use the `)
- to create a list use '-' in front of evey row
 - [ ] how to create task lists? (use '-[ ]' in front of the line and don't forget the empty space)
 - [x] and if task done? (use '- [x]')
 
 #### React and deploying on heroku
 I had the problem, the react code I created didn't work as I tried to deploy to [heroku](www.heroku.com).

The solution was to change some code in **package.json** of my react project.
I had to change in the scripts section 
`  "scripts": {
    "start": "react-scripts start",` to 
    `  "scripts": {
    "start": "serve -s build",`.
    
  #### How to change style in react (for example depending of a variable)
  
  ` <div
        className="projProgress"
        style={{
          height: projects[id].progress * 100 + "%",
        }}
      ></div> `
      
  #### You want to use some sound in your react?
  
  Check this [page](https://joshwcomeau.com/react/announcing-use-sound-react-hook/#installation)
  Everythin you have to do is to import the `import useSound from 'use-sound';`, then import your sound file `import boopSfx from '../../sounds/boop.mp3';`, write a small function in your hook `const [play] = useSound(boopSfx);` and put where you wish the action `<button onClick={play}>Boop!</button>;`. And you already have your first sound effect.
      
      
