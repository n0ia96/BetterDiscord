## Throughout the time that I've been using BetterDiscord, I've done some fixes and new code snippets to make Discord the way I wanted.

#### Here I'll share some of them so you guys can enjoy them as well.

----

## Better pings
This is one of my latests code snippets
Basically it changes the red pings of Discord to be... better ahah

```
/* - BETTER PINGS - */
.theme-dark .guilds-2JjMmN .listItem-3SmSlK .lowerBadge-3WTshO, .theme-dark .guilds-2JjMmN .listItem-3SmSlK .upperBadge-1V6Iyi {
    --pad: 100%;
    width: var(--pad);
    height: var(--pad);
    position: absolute;
    border: solid rgba(255, 0, 0, 0) 1px;
    z-index: 0;    
    display: grid; 
    grid-auto-columns: 1fr; 
    gap: 0px 0px; 
    justify-items: center; 
    align-items: center; 
}

div.numberBadge-37OJ3S.base-3IDx3L.eyebrow-132Xza.baseShapeRound-3epLEv {
    position: relative !important;
    padding-right: 0 !important;
    margin-left: auto !important;
    margin-top: auto !important;
    transform: rotateZ(-12deg) translateX(0vw);

    opacity: .8;
    z-index: 0;
    animation: .8s infinite alternate cubic-bezier(0.45, 0.05, 0.55, 0.95) pin-alert;
}
@keyframes pin-alert {
    from {
        transform: rotateZ(-12deg) translateX(0vw);
    } to {
        transform: rotateZ(12deg) translateX(.1vw);
    }
}
div.numberBadge-37OJ3S.base-3IDx3L.eyebrow-132Xza.baseShapeRound-3epLEv::after {
    content: "";
    position: absolute;

    width: 100%;
    height: 100%;
    right: 0;
    bottom: 0;
    opacity: 1;
    background-color: rgba(255,20,30,1);
    border-radius: 50%;
    z-index: -1;

    filter: blur(8px);
}

.lowerBadge-3WTshO::before {
    content: "᲼";
    position: absolute;
    z-index: -1;
    text-align: center;

    width: 92%;
    height: 92%;
    right: 0;
    bottom: 0;
    margin: auto;
    border: solid rgba(255,255,255,.2) .1vw;
    background: linear-gradient(160deg, rgba(255,255,255,0.08) 50%, rgba(0,0,0,0) 50%);
    border-radius: 50%;
    filter: blur(4px) !important;
    
}
.icon-3AqZ2e {
    object-fit: cover;
}
.lowerBadge-3WTshO::after {
    content: "᲼";
    position: absolute;
    z-index: -2;
    text-align: center;

    padding: 0;
    width: 95%;
    height: 95%;
    margin: auto;
    border:solid rgba(255,255,255,.02) 2px;
    background-color: rgba(255,255,255,.05);
    filter: blur(1px) !important;
    border-radius: 50%;

    animation: .9s infinite alternate glownoti;
}
@keyframes glownoti {
    from {
        filter: blur(100px) !important;
        background-color: rgba(255,255,255,.05);
    }
    to {
        filter: blur(1px) !important;
        background-color: rgba(255,255,255,.0);
    }
}
```
(Just paste the code into your BetterDiscord custom CSS file)