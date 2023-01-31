# NoteTaker

# Table of Contents
- Description
- Installation Instructions
- GitHub Account
- Contacts
- Images
- Code Snippets
- Resources
- Credits


# Description
This application was created to help keep track of writing, adding and deleting your saved notes.
The app will use an express backend, it will then save and retrieve note data from a JSON file in the db folder.

# Installtion Instructions
- Make sure `node.js` is installed in your machine
- Since the `package.json` was already included with the Note Taker repo, please
make sure to run `npm install` command in the terminal while in the root directory to install all required mods/packages
- Then run `node server.js` to start the server

# Github Account
- [GitHub](https://github.com/ashrean)
- [Deployed Heroku Link](https://hw11-note-taker1.herokuapp.com/)

# Images
![alt text](./public/assets/images/Screenshot%202023-01-30%20at%2011.20.36%20PM.png)

# Contacts
- [Email](sese.ashrean@gmail.com)
- [Linkedin](https://www.linkedin.com/in/ashleyrean/)

# Code Snippets
```
    addNote(note){
        const { title, text } = note;

        if(!title || !text) {
            throw new Error('Title and Text cannot be blank');
        }

        const newNote = { title, text, id: uuid() };
        return this.getNotes()
            .then((notes) => [...notes, newNote])
            .then((updatedNotes) => this.write(updatedNotes))
            .then(() => newNote);
    }
```
# Resources
- Class Activites
- [Heroku Documentation](https://devcenter.heroku.com/categories/reference)

# Credits
- Andrew M. (Tutor)
