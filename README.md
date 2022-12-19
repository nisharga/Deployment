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

<h2>BackEnd Code Deploy on Railway.app (Sign up+ Email Verify + Login)</h2> 
New Project >> github connect <br/>

https://railway.app/dashboard

New Project >> Deploy from GitHub repo <br/>
(All Repo show here from github) <br/>



1. Select the server side code repo, <br/>
2. Add Variables (Here you add your Environment Variables) <br/>
3. Click Deployments and wait until it finished <br/>
4. When Success go Setting >> Domains >> Generate Domain <br/>
5. Open domain in the new tab, wait some momont, and you get your backend live <br/>


Every time change automatic it will update via github. just you need to update github code. <br/>
Code Change: git add . git commit -m "commit" git push <br/>
wait 2 minutes and then see result on ui. <br/>
