# Noemi's Vinyl collection

I've been wanting to list my vinyls in some way for quite a while now and it just seemed to suit this flexbox-excercise.

## The problem

The flexbox-model worked out quite well i guess. For the phone screen it's still quite small and am not totally happy with the design. I'd work more on that if I had more time. The website I published by netlify took a while to load all pictures, but I think I could work that out by scaling down the sizes
I also wanted to include a linked overview (A-Z) so I can jump directly to artists in the end of the alphabet. I could solve this by linking the letters A-Z to the reffering flex-box-child. It turned out like I imagined it, but not sure if this is the easiest and clearest way to go. I wish I could include a linked box to the top of the website, that is fixed to the site even when scrolling, but couldn't make that work.
What I also wanted to try out was a hovering effect, so that when the curser hovers over the album cover, the artist and albumtitle turn up. But I couldn't figure that out. It destroyed the whole flexbox-style I've been working on for quite a while, so I deleted it again:) This is what I tried:

html:
      <section class="flex-parent">
      <div class="flex-child a"><h3 id="a.">a.</h3></div>
      <div class="flex-child allan">
        <div class="image">
        <img class="img" src="./Bilder/allan kingdom - lines.JPG" alt="alan kingdom">
        <div class="img_overlay">
            <div class="artist">allan kingdom</div>
            <p class="title">
              lines
css:
      position: relative;
      width: 250px;
    }
    .img {
      display: block;
      width: 100%;
    }
    .img_overlay{
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.6);
      color: black;
      font-family: permanent marker;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transition: opacity 0.25s;
    }
    .img_overlay > * {
      transform: translateY(20px);
      transition: transform 0.25s;
    }  
    .img_overlay:hover{
      opacity: 1;
    }
    .img_overlay:hover > * {
      transform: translateY(0px);
    }
    .artist{
      font-size: 2cm;
      font-weight: bold;
    }
    .title{
      font-size: 1.25cm;
      margin-top: 0.25cm;
    }

## View it live

https://angry-morse-a144db.netlify.app/#b
