### How can we build our customised button with `pop-up effect` while clicking over it ?
- I know there are tons of TailwindCSS component based library, where you can installed and attach some required plugin to `tailwind.config.js` file and you get those component.
- But in some use case, it becomes important to build own customized component (say Button which pop-up on click only), which we can achieve in TailwindCSS. 
- So while figuring out this stuff to implement in my current professional project, I found some useful insights.

So below👇🏼 is demonstration of customized button in `version 3` which I mean:

![btn-tailwind-v3](https://user-images.githubusercontent.com/71059909/158018311-0f143684-aad6-4f33-8f97-0467c74eb590.gif)

- Here is code: 
```
<div class="h-screen bg-white flex items-center justify-center">
  <button class="active:scale-90 transition duration-150 ease-out bg-green-200 hover:opacity-80 text-lg rounded w-64 p-2">
    HIRE ME
  </button>
</div>
```
- In order to bring that bouncing effect, don't use `animate-bounce` else it will always keep bouncing.
- Main take-away CSS `className` is `active:scale-90 transition duration-150 ease-out`.
- Click on the [Link-v3](https://play.tailwindcss.com/FGJ25Z771I) to see live example.
- They key difference after `version 3` is that you don't have to put a lot stuff in `tailwind.config.js`

But, like me most of you might have been using `version 2`, so the above stuff won't work. And you don't have upgrade to `V3` immediately. So below👇🏼 is the solution for it

![btn-tailwind-v2](https://user-images.githubusercontent.com/71059909/158018904-612c9f7f-0b98-4ab7-91a3-48bd4a84756f.gif)

- The code for button is same as above, only difference is to add few code 👇🏼 in `tailwind.config.js`
```
variants: {
      extend: {
         scale: ["active"],
       }
    }
```
- Click on the [Link-v2](https://play.tailwindcss.com/nDGL9p0Efz?file=config) for `V2`.

Lastly special✨ credit🙏🏼 to 👉🏼[Avi Avinav](https://github.com/AviAvinav) in helping me.





