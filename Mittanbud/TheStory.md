## The Mittanbud Story
So, let me tell you how this all started.
It was 2008. I had just started as a consultant at this little venture called DinePenger. There were three of us — Frode Ludviksen, Håvard Bungum, and me. VG, Norway's biggest newspaper, had hired us to build digital solutions. We had a budget, a deadline, and a lot of energy. What we didn't have was luck.
Almost overnight, the financial crisis hit. DinePenger didn't slowly fade away — it just died. Like someone pulled the plug. Six months of work, gone.
But we didn't go home. We started building something new.

## The Idea
The idea was pretty simple, actually. Everyone knows the old yellow pages — you look up who's out there and you call them. We wanted to flip that completely around. You describe what you need fixed, and then the carpenters, electricians, plumbers — whoever — they come to you and say they can do it. Based on the work they've done before, you pick whoever you feel most comfortable with.
Simple, right? Looking back, yes. At the time, it felt like a bet.
We built the first version on a basic LAMP stack — Linux, Apache, MySQL, PHP. Very standard for 2008. At one point we had a consultant come in who really wanted us to build the whole thing in Perl. I haven't heard anyone mention that language since. I'm glad we didn't listen to him.
Three months later, we had something to show.
And you have to remember what the web looked like back then. Mobiles existed, but mobile internet basically didn't. Websites were designed for 640x480 pixels. And JavaScript? Half the Norwegian companies out there had IT departments that treated JS like a virus and just blocked it. We started implementing it on the frontend and quickly realized a huge chunk of our users couldn't even run it. That was fun to discover.
We adapted. We waited. When jQuery came along and made JavaScript feel safe enough for the corporate world, we were ready.

## Free, on Purpose
For the first year or so, we made Mittanbud completely free for businesses. That wasn't us being naive — that was the strategy. Create real value first. Get tradespeople to actually want to use it. Then think about money.
While we were doing that, we spotted a competitor: Anbudstorget.no. They were already offering basically the same service. So we thought — why compete? Let's just buy them. We tried. They said no. And not just no — they told us they were so far ahead of us that we'd never catch up.
What they didn't think about was VG.
Every time there was an unused ad slot on VG — one of the most visited sites in Norway — Mittanbud was there. Almost free, at least we got a lot for our money. The exposure was relentless. I think it took us five or six months before we had surpassed Anbudstorget. Their head start didn't count for much against Norway's biggest newspaper pushing us every single day.

## The Coffee That Changed Everything
Then came the moment I still think about.
Finn.no — think of it as Norway's Craigslist, eBay and Zillow rolled into one, the single biggest website in the country — announced they were launching Finn Oppdrag. A direct competitor. And here's the part that still makes me laugh: both Finn and VG were owned by Schibsted. The same parent company that backed us was now funding the thing that was supposed to kill us.
Before they launched, they invited Håvard and me in for a meeting. The message was clear: you're small, you're insignificant, just give up and let Finn Oppdrag take the market. That was basically it.
After that meeting, Håvard and I walked out and found a coffee bar just outside Finn's offices. We sat down. Neither of us really wanted to say what we were thinking.
But we agreed on one thing: we still had some time. We weren't ready to give up. If nothing else, let's be a thorn in their side.
We finished our coffees and got back to work.
Five years later, Finn Oppdrag shut down. We took over their company.
Not bad for a couple of guys who started on the ashes of a financial crisis.


## What Comes After Winning
That was 2015. While we were wrapping up the migration of data from Finn Oppdrag into Mittanbud, I was about to head out on paternity leave with my second kid. Six months of diapers, sleepless nights, and — somewhere in between — a lot of thinking.
Just before I left, Håvard and I had a quiet little meeting. There wasn't really a plan yet, but the message was clear: we had won. We were the biggest in Norway. Now what? We needed to grow, and we needed a platform that could actually support that growth.

So that's what I spent the next six months doing — reading, sketching, and thinking about how we could build something flexible enough to house basically whatever we wanted. Because the old Mittanbud had become what we used to call a lappeteppe — a patchwork quilt of solutions, stitched together under pressure while we were busy fighting Finn. There had never been time to step back and restructure properly. The codebase was full of really solid, optimized work — built by a small but sharp team: John Larsen, Magne Dyrnes, Tor Espedal, Erik Bergh, and me. But it was optimized for being one site doing one thing. A general, fits-all platform it was not.
The vision was a microservice architecture. Something that scaled not just by throwing bigger servers at the problem, but by adding more servers and having them work together. It was what all the big players were doing.
I was going to do it with five people. Who already had full-time jobs keeping the existing Mittanbud alive.

Yeah. That wasn't going to work.

## Building While the House Is Still Standing
We started with the administration system. The choice of language was easy — PHP. We knew it well, it was fast, reliable, and if you don't mind a bit of weird C-style syntax, it's genuinely a great tool. Node.js had just arrived on the scene, but at the time two factions in the Node community couldn't agree on direction, and suddenly there were two versions running in parallel. That mess sorted itself out about a year later, but we weren't going to bet the company on it.
I hired one new person — Petter Harsem, fresh out of school — and we also brought in a bachelor student group, lead by Håvard Melvin Gillebo Hjelvik. Together, we built the first version of the admin system in about four months.

But by then, the company's ambitions had shifted. The admin system didn't end up as the backend for Mittanbud. Instead, it became the engine for our ads service. Because we were still owned by Schibsted — a major media group — we had found a clever way to split large national ad buys into dozens of geo-targeted, specialized ads. Instead of one business paying 50,000 kr for a single ad on VG, you had fifty different businesses each paying around 1-3,000 kr for something far more targeted. High-demand, high-volume, and suddenly we needed both a sales system and an admin layer to manage all of it.

We were building that and trying to rebuild Mittanbud at the same time.

## The Platform That Never Shipped
About a year in, we acquired eiendomsmeglersiden.no — a site out of Bergen where a small team had built a tender platform for real estate. Just like that, we needed to launch a whole new website on top of the platform, with the admin system — now called Melvis, named after Håvard Melvin who was being trained up as tech lead on it — underneath it all.

So now we were building Melvis, running the ads service, trying to rebuild Mittanbud, and launching a real estate platform. With basically the same number of people.

It became something of an internal meme: we were never going to finish the new Mittanbud platform. And honestly? The meme was earned. We kept biting off more than we could chew. 

Eiendomsmeglerguiden.no became meglersiden.no — which was actually the first real frontend release on the new platform, now built with React. Then came Varmepumpe123.no. Then ProjectPluss.no.
Each one was a win. Each one was also another reason the core Mittanbud rebuild kept getting pushed back.
We were building the plane while flying it, launching new products off the wing, and somehow still in the air.


