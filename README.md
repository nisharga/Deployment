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

(Don't Forget to Replace New Code: Open frontend code via VSCode. Then Edit >> Find in Files or 
CTRL + SHIFT + H . One click replace all code
after that just give one command npm run build and you get build folder)




(Sign up + Email Verify + Login)

https://app.netlify.com/ 

Add New Site > Deploy Manually

DRAG and DROP your build folder. DONE!!!


Route Related Issue on frontend _redirects file peast on public folder.(you will find the file in this git repo)

<hr/>

<h2>FrontEnd Code Deploy on vercel</h2>


https://vercel.com/dashboard (Sign up+ Email Verify + Login)

(Make sure already vercel install on PC. If not then Don't forget to npm i -g vercel command to vercel setup your PC)

0.in npm comand vercel (then login)
1.Set up and deploy: Y
2.Select your vercel account email.
3.Link to existing project: N
4.Whats your project name: (Enter)
5.In which directory is your code located: ./ (Enter)
6.Want to modify these settings - N


Everytime changing just command vercel





