# CS 260 Notes

[My startup - Simon](https://simon.cs260.click)

## Helpful links

- [Course instruction](https://github.com/webprogramming260)
- [Canvas](https://byu.instructure.com)
- [MDN](https://developer.mozilla.org)

## AWS

This was kind of confusing, but I figured it all out. Website is up and running. 

## Caddy

No problems worked just like it said in the [instruction](https://github.com/webprogramming260/.github/blob/main/profile/webServers/https/https.md).

## HTML

Using html isn't too bad, though I am learning how to use it. Though, it's pretty straightforward. I just don't know what the things in the future will do, so I'm not sure really how to plan for that. I'm not sure if I'm missing something in the html that I've assumed will be something later on. 

## CSS

This took a couple hours to get it how I wanted. It was important to make it responsive and Bootstrap helped with that. It looks great on all kinds of screen sizes.

Bootstrap seems a bit like magic. It styles things nicely, but is very opinionated. You either do, or you do not. There doesn't seem to be much in between.

I did like the navbar it made it super easy to build a responsive header.

```html
      <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
          <a class="navbar-brand">
            <img src="logo.svg" width="30" height="30" class="d-inline-block align-top" alt="" />
            Calmer
          </a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <a class="nav-link active" href="play.html">Play</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="about.html">About</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="index.html">Logout</a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
```

I also used SVG to make the icon and logo for the app. This turned out to be a piece of cake.

```html
<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg">
  <rect width="100" height="100" fill="#0066aa" rx="10" ry="10" />
  <text x="50%" y="50%" dominant-baseline="central" text-anchor="middle" font-size="72" font-family="Arial" fill="white">C</text>
</svg>
```

## React Part 1: Routing

Setting up Vite and React was pretty simple. I had a bit of trouble because of conflicting CSS. This isn't as straight forward as you would find with Svelte or Vue, but I made it work in the end. If there was a ton of CSS it would be a real problem. It sure was nice to have the code structured in a more usable way.

## React Part 2: Reactivity

This was a lot of fun to see it all come together. I had to keep remembering to use React state instead of just manipulating the DOM directly.

Handling the toggling of the checkboxes was particularly interesting.

```jsx
<div className="input-group sound-button-container">
  {calmSoundTypes.map((sound, index) => (
    <div key={index} className="form-check form-switch">
      <input
        className="form-check-input"
        type="checkbox"
        value={sound}
        id={sound}
        onChange={() => togglePlay(sound)}
        checked={selectedSounds.includes(sound)}
      ></input>
      <label className="form-check-label" htmlFor={sound}>
        {sound}
      </label>
    </div>
  ))}
</div>
```
## Midterm Study:
"""CSS NOTES:

      1.	In the following code, what does the link element do?
      Links to another page. Could be CSS, could be bootstrap.
      2.	In the following code,  what does a div tag do?
      The dive tag divides the code into different sections. 
      3.	In the following code, what is the difference between the #title and .grid selector?
      #title is for a specific id, or element. .grid is for changing many things within a class.
      4.	In the following code, what is the difference between padding and margin?
      Padding changes space within the border of the element, margin changes space outside the border of the element.
      5.	Given this HTML and this CSS how will the images be displayed using flex?
      6.	What does the following padding CSS do?
      7.	What does the following code using arrow syntax function declaration do?
      Makes it more compact and concise.
      8.	What does the following code using map with an array output?
      Mapping applies the function to each thing in the array.
      9.	What does the following code output using getElementByID and addEventListener?
      Gets a specific element. “Listens” for an event to happen like a mouse click, mouse hover, button press, etc.
      10.	What does the following line of Javascript do using a # selector?
      Selectors are used to target and manipulate elements in the DOM (Document Object Model).
      11.	Which of the following are true? (mark all that are true about the DOM)
      The Document Object Model (DOM) is a programming interface for web documents, treating an HTML or XML document as a tree structure of objects (nodes). These nodes have various properties that allow developers to interact with and manipulate the document's structure, style, and content. 
      12.	By default, the HTML span element has a default CSS display property value of: 
      By default, the HTML <span> element has a CSS display property value of inline.
      
      13.	How would you use CSS to change all the div elements to have a background color of red?
      Id, Class, or a CSS on all div elements.
      14.	How would you display an image with a hyperlink in HTML?
      <img src="w3html.gif" alt="W3Schools.com" width="100" height="132">
      15.	In the CSS box model, what is the ordering of the box layers starting at the inside and working out?
      Content, Padding, Border, Margin 
      16.	Given the following HTML, what CSS would you use to set the text "trouble" to green and leave the "double" text unaffected?
      17.	What will the following code output when executed using a for loop and console.log?
      console.log() is a built-in JavaScript function used to output messages, variables, or expressions to the browser's developer console or a runtime environment's debugging console. It is a fundamental tool for debugging and understanding the execution flow of JavaScript code.
      18.	How would you use JavaScript to select an element with the id of “byu” and change the text color of that element to green?
      19.	What is the opening HTML tag for a paragraph, ordered list, unordered list, second level heading, first level heading, third level heading?
      <p>, <ol>, <ul>, <li>, <h1>
      20.	How do you declare the document type to be html?
      <!DOCTYPE html>
      21.	What is valid javascript syntax for if, else, for, while, switch statements?
      if (condition) {
        // Code to execute if condition is true
      } else if (anotherCondition) {
        // Code to execute if condition is false and anotherCondition is true
      } else {
        // Code to execute if both conditions are false
      }
      
      for (initialization; condition; increment) {
        // Code to execute repeatedly as long as the condition is true
      }
      
      while (condition) {
        // Code to execute repeatedly as long as the condition is true
      }
      
      switch (expression) {
        case value1:
          // Code to execute if expression === value1
          break; // Important to prevent "fall-through"
        case value2:
          // Code to execute if expression === value2
          break;
        default:
          // Code to execute if no case matches
      }
      
      22.	What is the correct syntax for creating a javascript object?
      let myObject = {
        property1: "value1",
        property2: 123,
        method1: function() {
          console.log("This is a method.");
        },
        nestedObject: {
          nestedProperty: true
        }
      };
      
      23.	Is it possible to add new properties to javascript objects?
      yes
      24.	If you want to include JavaScript on an HTML page, which tag do you use?
      <script>
      25.	Given the following HTML, what JavaScript could you use to set the text "animal" to "crow" and leave the "fish" text unaffected?
      
      26.	Which of the following correctly describes JSON?
      JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write, and easy for machines to parse and generate. It is often used to transmit data between a server and a web application, as well as between different parts of an application.
      JSON Syntax
      JSON is built on two structures:
      1.	A collection of name/value pairs: In various languages, this is realized as an object, record, struct, dictionary, hash table, keyed list, or associative array.
      2.	An ordered list of values: In most languages, this is realized as an array, vector, list, or sequence.
      Example of JSON
      {
      "employees": [
      {"firstName": "John", "lastName": "Doe"},
      {"firstName": "Anna", "lastName": "Smith"},
      {"firstName": "Peter", "lastName": "Jones"}
      ]
      }
      
      27.	What does the console command chmod, pwd, cd, ls, vim, nano, mkdir, mv, rm, man, ssh, ps, wget, sudo  do?
      Here are the descriptions of the provided Linux commands:
      •	chmod: Changes file permissions (read, write, execute) for the owner, group, and others.
      Code
          chmod 755 myfile.sh # Grants owner read, write, execute; group and others read, execute.
      •	pwd: Prints the current working directory, showing the full path from the root.
      Code
          pwd
      •	cd: Changes the current working directory.
      Code
          cd /home/user/documents # Changes to the specified directory.
          cd .. # Moves up one directory.
      •	ls: Lists the contents of a directory.
      Code
          ls # Lists files and directories in the current directory.
          ls -l # Provides a detailed list with permissions, ownership, size, etc.
      •	vim: A powerful, highly configurable text editor.
      Code
          vim filename.txt # Opens filename.txt in Vim.
      •	nano: A simple, user-friendly text editor.
      Code
          nano filename.txt # Opens filename.txt in Nano.
      •	mkdir: Creates new directories.
      Code
          mkdir mynewdirectory # Creates a new directory named mynewdirectory.
      •	mv: Moves or renames files and directories.
      Code
          mv oldname.txt newname.txt # Renames oldname.txt to newname.txt.
          mv file.txt /path/to/destination # Moves file.txt to the specified destination.
      •	rm: Removes files or directories.
      Code
          rm myfile.txt # Removes myfile.txt.
          rm -r mydirectory # Recursively removes mydirectory and its contents.
      •	man: Displays the manual page for a given command.
      Code
          man ls # Displays the manual page for the ls command.
      •	ssh: Securely connects to a remote server.
      Code
          ssh username@remote_host # Connects to remote_host as username.
      •	ps: Displays information about running processes.
      Code
          ps aux # Shows all running processes with detailed information.
      •	wget: Retrieves files from the web.
      Code
          wget https://example.com/file.zip # Downloads file.zip from the given URL.
      •	sudo: Executes a command with superuser privileges.
      Code
          sudo apt update # Updates package lists with root privileges.
      
      28.	Which of the following console command creates a remote shell session?
      The ssh command
      29.	Which of the following is true when the -la parameter is specified for the ls console command?
      Lists hidden files
      30.	Which of the following is true for the domain name banana.fruit.bozo.click, which is the top level domain, which is a subdomain, which is a root domain?
      The parts are: the protocol https://, the subdomain www, the domain name example.com, the path /path/to/page.html, and the fragment #section. 
      31.	Is a web certificate is necessary to use HTTPS.
      Yes, a web certificate is necessary to use HTTPS, as it provides the encryption and authentication needed to create a secure connection
      32.	Can a DNS A record can point to an IP address or another A record.
      No, a DNS A record cannot point to another A record; it must always point directly to an IPv4 address
      33.	Port 443, 80, 22 is reserved for which protocol?
      Port 443 is used for HTTPS (secure web traffic), port 80 is used for HTTP (unsecured web traffic), and port 22 is used for SSH (Secure Shell for secure remote access)
      34.	What will the following code using Promises output when executed?
      let myPromise = new Promise((resolve, reject) => {
        // Simulate an asynchronous operation (e.g., fetching data)
        setTimeout(() => {
          let success = true; // Imagine this comes from an API call result
      
          if (success) {
            resolve("Data fetched successfully!"); // Fulfill the promise
          } else {
            reject("Failed to fetch data."); // Reject the promise
          }
        }, 2000);
      });
      const delay = (msg, wait) => {
        setTimeout(() => {
          console.log(msg, wait);
        }, 1000 * wait);
      };
      
      new Promise((resolve, reject) => {
        // Code executing in the promise
        for (let i = 0; i < 3; i++) {
          delay('In promise', i);
        }
      });
      
      // Code executing after the promise
      for (let i = 0; i < 3; i++) {
        delay('After promise', i);
      }

"""
