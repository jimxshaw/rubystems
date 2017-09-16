# User Interface (UI) Specification (Spec)
Intended for the desktop web application with mobile browser responsiveness in mind.

## Pages

### Home page (/)

- Navbar: logo/name top left, menu items on the right
  - logo/name top left renders (/)
  - top righ: stems | about
    - stems renders (/stems)
    - about renders (/about)
    
- Footer: Copyright/license notice and GitHub link

- Content: snazzy deseign with big words and modern icons

### About page (/about)

- Lists the motivation, purpose, and vision of RubyStems

### Stems page (/stems)

- Will be an in-browser application, built with React components.
  - Advancing to each stem shouldn't generate a new url.
- Top header: RubyStems logo or name on top left | { lang || topic } + { collection if exists? } in center
- Footer: hamburger menu with stem name on bottom left | previous button | progress indicator | next button

#### Inspiration
[How to create a user interface specifications document (UI Spec)](https://www.startuprocket.com/articles/how-to-create-a-user-interface-specifications-document-ui-spec)
