<h2>Video Tutorial</h2>

https://www.loom.com/share/bcee9f6ddd4245c6a4740c969f305d84

<hr/>

<h2>Backend Deploy on Render .com Site </h2>

First go to render.com (Sign up+ Email Verify + Login)<br/>
Web Service >> Github connect <br/> <br/>

After Login go to Web Services >> New Web Service <br/>
Search the repo name from github. And Click Connect<br/>

  <code>Name: Give A Name (Github same repo name would better)</code></br>
  <code>Region: (default)</code></br>
  <code>Branch: (default)</code></br>
  <code>Root Directory: (default)</code></br>
  <code>Environment: Node</code></br>
  <code>Build Command: (default)</code></br>
  <code>Start Command: node index.js</code></br>

  (My file name is index.js, if you have other name try out yourself)</br>

Then Advanced: Add <code>Environment Variables</code></br>

Finally, Click on "Create Web Service" it will take upto 2 minutes.After successfully deploy you get your server link.</br>

Every time change automatic it will update via github. just you need to update github code.</br>
<code>git add . </code></br>
<code>git commit -m "commit" </code></br>
<code>git push</code></br>

wait 2 minutes and then see result on ui.

<hr/>

<h2>FrontEnd Deploy on Netlify</h2> 

(Don't Forget to Replace New Code on frontend code: Open frontend code via VSCode. Then Edit >> Find in Files or <code>CTRL + SHIFT + H </code>.
  
 One click replace all code.</br> Route Related Issue on frontend <code>_redirects</code> file peast on public folder. (you will find the file in this git repo)</br> after that just give one command <code>npm run build</code> and you get build folder)</br> after that go https://app.netlify.com/ (Sign up + Email Verify + Login)</br> <code>Add New Site > Deploy Manually</code> </br> DRAG and DROP your build folder. DONE!!! <hr/> <h2>FrontEnd Code Deploy on vercel</h2> https://vercel.com/ (Sign up+ Email Verify + Login)</br> (Make sure already vercel install on PC. If not then Don't forget to <code>npm i -g vercel</code> command to vercel setup your PC, lifetime only once)</br></br> 0.in npm comand <code>vercel</code> (then login)</br> <code>1.Set up and deploy: Y</code></br> <code>2.Select your vercel account email.</code></br> <code>3.Link to existing project: N</code></br> <code>4.Whats your project name: (Enter)</code></br> <code>5.In which directory is your code located: ./ (Enter)</code></br> <code>6.Want to modify these settings - N</code></br> Everytime changing just command <code>vercel</code>

<hr/>

<h2>BackEnd Code Deploy on Railway.app </h2> 
(Sign up+ Email Verify + Login)

New Project >> github connect <br/>

https://railway.app/dashboard

New Project >> Deploy from GitHub repo <br/>
(All Repo show here from github) <br/>



1.<code> Select the server side code repo,</code> <br/>
2.<code> Add Variables (Here you add your Environment Variables)</code> <br/>
3.<code> Click Deployments and wait until it finished </code> <br/>
4.<code> When Success go Setting >> Domains >> Generate Domain </code> <br/>
5.<code> Open domain in the new tab, wait some momont, and you get your backend live </code> <br/>


Every time change automatic it will update via github. just you need to update github code. <br/>
Code Change: git add . git commit -m "commit" git push <br/>
wait 2 minutes and then see result on ui. <br/>


### Backend Next Level Backend Host On Vercel
#### Step 0: create a vercel.json file in root
#### Step 1: Copy this code and peast on vercel.json

```bash
{
  "version": 2,
  "builds": [
    {
      "src": "src/server.ts",
      "use": "@vercel/node"
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "src/server.ts"
    }
  ]
}
```

Inside Src declire the path. My server.ts file located inside src thats why i write src/server.ts also in dest

#### Step 2: Login Vercel with CMD
```bash
vercel login
```
#### Step 3: After Login Vercel Then Type
```bash
vercel
```
#### Step 4: Answer these questions
Set up and deploy: Y

Which scope do you want to deploy to?: Gmail

Link to existing project? [y/N] n

What’s your project’s name? (Type Name which will your URL)

In which directory is your code located? ./ Enter


#### Step 5: After Getting a Link Check a get route. If face issue login vercel with browser go to that project and see logs. (GlobalErrorHandler Common problem for hosting)
