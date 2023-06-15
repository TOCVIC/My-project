# My-project

In this guide we will be using Github Pages to create a simple website. But first, how does a website work? When you enter a website address in your computer’s browser, the browser makes a request to a remote server computer. If successful, the server returns HTML, CSS, and JS for the page requested which your browser then renders to your screen. In our case, Github Pages will be the remote server.

![image](https://github.com/TOCVIC/My-project/assets/86574097/272c8089-0a42-423b-b3cc-e4714644532a)


Step 1: Create a Github account
In your browser, go to github.com and create a free account. Github is a website that allows you to upload and share versioned code with others. It also supports simple website hosting (which we will be using today).

Step 2: Find the Maker Lab website template
Login and navigate to the Maker Lab Website Template on Github.

Step 3: Fork (copy) the template
Click the Fork button in the upper right of the screen. This will create your own personal copy of the project repository which you can then modify.
![image](https://github.com/TOCVIC/My-project/assets/86574097/36b2f9d4-36b6-4d70-b8e7-994f4340d0e1)


Step 4: Edit the website URL
Once you have forked the project, click the Edit button to the write of “Website URL” and update the URL to match your github username. Make sure to write this down! This is how you will be able to view and share your website with others.

Example URL (replace yourusername with your github username):

https://yourusername.github.io/simple-website-template

Step 5: Try to load your website URL
If you try to navigate to your URL right now, you will get a 404 Error: Not Found. We have to push some changes first to the gh-pages branch before Github will build our website.

Step 6: Edit index.html
Click index.html and then click the pencil icon to edit the file in the browser editor.
![image](https://github.com/TOCVIC/My-project/assets/86574097/9af6f340-0213-46e4-b6e4-79e5159882df)



Step 7: Change the page title and heading
In the HTML editor look for the title tag: <title>Your title here</title> Change the text inside the title tags, without modifying the tags themselves. Similarly, find the h1 heading tag and carefully change the text inside of the h1 tags:  <h1>Simple Website</h1>

![image](https://github.com/TOCVIC/My-project/assets/86574097/029aa4a3-d374-4c1d-918d-fdc3f11d95ba)

For more examples of tags, see the “Common HTML Tags” table at the end of this guide.

Step 8: Commit your changes
Scroll down and click Commit changes. This will save and push the changes you made to the gh-pages branch. Git uses branches and commits to manage different versions of your files.
![image](https://github.com/TOCVIC/My-project/assets/86574097/a3046cd5-ae00-46ab-a4d4-962db5be4f99)

Step 9: Wait for your site to build!
After a commit it will take about 3-4 minutes to deploy your site. You can monitor the status of your build by clicking the “Environment” tab. After a few minutes, visit your website URL to see your new site.

Step 10: Upload new background image
Now let’s upload a new background image. Search for a large image (~1024 pixels wide), download it to your computer, and rename it background.jpg. Your image must be named background.jpg before uploading in order to overwrite the original image. If your image is a .png, use GIMP to convert it to .jpg.

In Github, click Uploadfiles to upload your new background.jpg. Don’t forget to scroll down and click “Commit changes” to push your changes to the gh-pages branch. Again, it usually takes about 3-4 minutes for Github to build and deploy your changes.

![image](https://github.com/TOCVIC/My-project/assets/86574097/b1473373-7de6-4c89-9f0e-3f4d694af110)


Congratulations! You made a website!
Yeah! You did it! Now you can share your website link with your friends so they can see your website too.


Tools used
GitHub 
HTML
JS
CSS


# simple-website-with-blog

> A simple website with a blog

`simple-website-with-blog` is a simple [Node.js](https://nodejs.org/) web application for static content that includes a blog.
It was created as the basis for [my own website](https://dlaa.me/), but everyone is welcome to use it.
The implementation strives to be simple and free of unnecessary dependencies.

## Goals

- An easy way to create a simple, secure website with a blog
- Support for text-based and photo-based blog formats
- Easy authoring in HTML, Markdown (with code formatting), or JSON
- Ordering of posts by publish date or content date
- Easy customization of site layout and formatting
- High resolution (2x) support for photo blog images
- Support for Windows and Linux hosting with Node.js
- Simple post format that separates content and metadata
- Ability to author hidden posts and schedule a publish date
- Ability to create posts that never show up in the timeline
- Support for archive links and tagging of posts by category
- Quick search of post content, including simple search queries
- Automatic Twitter and Open Graph metadata for social media
- Automatic cross-linking of related posts
- No JavaScript requirement for client browsers

## Structure

- `/app.js` Entry point for the application, configures the server and static content
- `/blog.js` Implementation of the blog, archives, tags, search, and RSS
- `/config.js` Environment variables used to control basic behavior
- `/sites/shared.js(x)` Blog layout code shared by the sample sites
- `/sites/sample-text/render.js(x)` Blog layout code for the sample text blog
- `/sites/sample-text/static/...` Static files and directories for the sample text blog
- `/sites/sample-text/posts/...` Post metadata and content for the sample text blog
- `/sites/sample-photo/...` Sample photo blog
- `/sites/test/...` Test site for running unit tests

## Instructions

1. Install Node.js
1. Fork and clone repository
1. Create directory under `/sites` or use one of the samples
1. Add static content to `/sites/yoursite/static`
1. Add post JSON and content under `/sites/yoursite/posts`
1. `npm install`
1. `npm run compile`
1. `npm start`
1. Open <http://localhost:3000/> and verify
1. Commit changes to repository
1. Deploy repository to hosting service

## Configuration

- `SWWB_SITE_ROOT` Set to specify the site to use when serving content (ex: `./sites/sample-text`)
- `SWWB_REDIRECT_TO_HTTPS` Set to `true` to redirect HTTP traffic to HTTPS and set an HSTS header
- `SWWB_SHOW_FUTURE_POSTS` Set to `true` to show posts with a publish date in the future (good when authoring locally)
- `SWWB_HOSTNAME_TOKEN` Set to change the replacement token for inserting host name in posts (RSS uses absolute URLs)
- `SWWB_ACME_CHALLENGE` Set to specify the ACME challenge for [Let's Encrypt](https://letsencrypt.org/) (ex: `abc.123,def.456`)

## Dependencies

| Project      | Home Page                                    |
|--------------|----------------------------------------------|
| Express      | <https://expressjs.com/>                     |
| React        | <https://reactjs.org/>                       |
| Helmet       | <https://helmetjs.github.io/>                |
| markdown-it  | <https://github.com/markdown-it/markdown-it> |
| highlight.js | <https://highlightjs.org/>                   |
| Lunr         | <https://lunrjs.com/>                        |
| rss          | <https://github.com/dylang/node-rss>         |

## Contributing

- Open issue, discuss proposal
- Fork and clone repository
- Change code and update tests
- `npm test`
- `npm run lint`
- Review changes
- Send pull request

## License

[MIT](LICENSE)
