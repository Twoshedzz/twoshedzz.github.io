---
title: Back on the AI wagon (again)
description: I've dabbled back into AI to help write code, again, this time it's apps.
author: twoshedzz
date: 2025-12-19 21:29:00 +0800
categories: [Blogging]
tags: [Bloodbowl, AI]
pin: true
math: false
mermaid: false
image:
  path: /assets/img/posts/2025-12-19-back-on-the-ai-wagon/builder-screenshot.jpg
  alt: A screen shot of a blood bowl roster builder app, produced in Claude and Cursor, published in GitPages.
---

I’d gone quiet on the coding and AI stuff.

Not intentionally — just distracted, busy, and probably a bit overwhelmed. I’d been obsessing over ChatGPT and GitHub Copilot for a while and hadn’t really looked at all the *other* tools that keep popping up. There are loads of them now. It all felt… confusing.

Then, at a recent works do, my interest was piqued again by a colleague who’d casually mentioned they’d *“made an app”* using **Lovable**.  


That stuck with me.

## Prodding Lovable on the train home

On the train back from London I decided to give Lovable a go. I asked it to make a **Blood Bowl roster creator**.

The prompt was (almost intentionally) crap.

I wasn’t trying to be precise — I was just prodding to see what would happen with a really open brief. I didn’t feed it any data. I didn’t explain the rules properly. I just… asked.

And honestly? It was impressive.

In seconds — *seconds* — it produced something passable:
<https://lovable.dev/projects/8bb887f1-2a82-46a5-9e58-bae676312fcb>

It wasn’t correct, or complete, or even especially good — but it existed. That alone was enough to hook me again.

## Falling into Claude

I did some light research after that, and **Claude** was recommended.  
By ChatGPT, amusingly enough.

I really liked the Claude interface straight away. It’s clean, calm, and easy to work with. I felt like I was making rapid progress almost immediately.

Before long, I’d got to this:
<https://claude.ai/public/artifacts/79290956-b0b0-43c7-a840-6efbde42a1f1>

Claude helped me scrape data from sites, mess around with layouts, even try background images. The flow was good. Iterative. Encouraging.

But I hit a limit.

Publishing.

Claude was essentially producing **one big JSX file**. Fine for experimentation, but not great if you want something more robust — separate data files, images, features you can grow over time.

## Taking the plunge with Cursor

That’s when I decided to take the plunge with **Cursor**.

You download it and suddenly you’re in something that feels a lot more like VS Code. Immediately more technical. More intimidating. More *real*.

The goal here was to build something a bit more solid:
- separate data files  
- images  
- room to add features  
- something that could actually be published properly  

Cursor helped a lot. It even rattled through setting up GitHub Pages publishing, so the app actually exists on the internet:

<https://twoshedzz.github.io/blood-bowl-roster/>

I hesitate to call it *my* app.

Is it my app?

I’ve vibe coded the whole thing. I haven’t written a single line of code myself. I’ve run a handful of terminal commands and that’s about it.

And yet… there it is.

## Things I think I’ve learned (or am learning)

A few reflections so far:

- **Jumping straight in works… at first**  
  I bundled in and started describing the roster builder. That got things moving quickly, and that was fine early on.

- **Small, well-defined features work better**  
  The best progress came when I started asking for very specific additions, one at a time.

- **You need to know when a feature is “done”**  
  I’ve lost features a couple of times when adding new ones. In Cursor I even asked it to create and run tests. At one point I asked it to refactor the code so teams lived in separate data files — it did this really well.  
  Two or three features later… everything was back in one file.  
  I don’t fully know how. It could be me getting confused with the Cursor interface and branches, but it’s something I’m trying to keep an eye on.

- **You have to pay**  
  AI is addictive. Honestly, very addictive.  
  It feels like being a product manager or MD running a tiny company with devs beavering away alongside you. Making something usable in minutes or seconds feels powerful — and fun.  
  But you hit cost ceilings and token limits *all the time*.

## What next?

There has to be a point now where I stop and actually **review the code** that’s been produced, and see what I understand myself.

I’d also really like to watch someone using Cursor who’s more experienced at coding *and* vibe coding. I’ve mostly stumbled around on my own, asking AI to interpret screenshots when I get stuck.

Part of me misses the days of sitting in an office with a team — being able to lean over and ask a colleague a question and learn something quickly, in real time.

This feels powerful. It also feels lonely.

More ramblings to come, I suspect.
