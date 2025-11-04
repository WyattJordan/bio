# Personal Website to Learn Web Dev 
Available at [wyattjordan.cc](www.wyattjordan.cc)

## Inspiration
Websites under 14kb load in the first round of the TCP slow start algorithm ([original blog](https://endtimes.dev/why-your-website-should-be-under-14kb-in-size/)). I decided to make my own (finally). Also [good post](https://medium.com/@moonshadowrev/how-i-finally-built-my-portfolio-site-under-14kb-a-chill-journey-inspired-by-a-random-youtube-45ef1008b483) by another person who went on this journey for their [portfolio website](moonshadowrev.me).

## Step 1 - Web Framework Selection
From the [2025 stack overflow developer survery](https://survey.stackoverflow.co/2025/technology#most-popular-technologies-comm-platform-prof) react and node.js are still wildly popular so want to use those tools as they are mature and will have more support. But keeping it under 14KB would be difficult with either. Apparently [preact](https://preactjs.com/) is a lighter version of react which will let me stay <14KB (per [blog post](https://medium.com/@moonshadowrev/how-i-finally-built-my-portfolio-site-under-14kb-a-chill-journey-inspired-by-a-random-youtube-45ef1008b483)). That blog post also mentioned Tailwind which I want to try out for nice customization right in html.

## Step 2 - Domain and Hosting
Purchased wyattjordan.cc domain for $8/yr for the next 10 years (expires in 2035). After brief google selected [Vercel](https://vercel.com/wyatt-jordans-projects/bio) for hosting.

Configure DNS routing on Vercel after purchasing domain on Cloudflare (See the [Vercel Migration Guide](https://vercel.com/guides/migrate-to-vercel-from-cloudflare#2.-migrating-custom-domains-with-zero-downtime)) and follow the same guide to setup SSL (actually this just fixed itself somehow 🤷🏼‍♂️). Also Vercel recommends not using [the cloudflare reverse in front of it](https://vercel.com/guides/cloudflare-with-vercel#using-cloudflare-as-your-dns-provider). 

## Preact
Vercel supports many frameworks but you do not deploy your own docker container. However Preact is supported and here is the [boilerplate code](https://github.com/vercel/examples/tree/main/framework-boilerplates/preact) for it (copied into this repo). Setting this up on my local system I'll use dev containers (docker) in vscode for local testing.

## Tailwind
Motivation for the creation of tailwind [blog post](https://adamwathan.me/css-utility-classes-and-separation-of-concerns/).

## High Level Goals
✅ Configure website using a default configuration provided by Vercel.  
✅ Make basic modification and test deployment
✅ Get basic preact custom build working and deploying to host (just used boiler plate)
✅ Make <14KB and keep it that way (basic preact app was only 3KB)

2. Settle on a basic design and color formatting
3. Write a basic bio and links to various pages (github, linkedin, etc)
4. Play around with delayed loading of images (placeholder boxes for image locations so under 14KB then fetch)
5. 


## Long-term things to try
[WebGPU](https://webgpu.github.io/webgpu-samples/?sample=helloTriangle#main.ts) (and instructions for user to enable it on different platforms), see [WebGPU fundamentals](https://webgpufundamentals.org/)

