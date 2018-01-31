---
layout: post
title:      "Bringing it all together"
date:       2018-01-31 18:06:09 +0000
permalink:  bringing_it_all_together
---


Up until this point it feels like a lot of the work I was doing within the curriculum was to complete different challenges. The Ruby Gem CLI was the first time that I got to do something from scratch and see where both the skills that I’ve learned and my creativity took me. It was a great feeling.

It took me awhile to decide what I wanted to do for the project. I found myself thinking about it long before I actually reached it. I was considering a lot of the blogs I enjoy but the problem for me was that it didn’t really allow for interaction or custom results. At the time my childhood home was for sale and I was looking at the listings in the area and I realized that the layout of results and the way the zip was queried into the URL was absolutely perfect for the CLI project.

I finally reached the Data Gem Assessment and watched all the videos. The first step was using bundler to create the proper file structure and dependencies for the Gem. Actually getting that to work was probably the hardest part for me. I laid out a hard coded CLI class that called through the console and with a lot of trial and error finally stopped getting LoadErrors. 

From this point forward I honestly felt clairvoyant. There aren’t many times that I had to slow down to think what to do next. Everything I had worked on up until this point was guiding me along in a seamless manner and it felt incredible. Once I had the CLI groundwork down I moved into scraping. I was lucky that realtor.com's css tags were so well done because it made it a breeze. I used all my knowledge of Pry and other debugging tools to verify the values of the data I was storing and was quickly ready to move on.

Next I had to create instances of listings from the data I was scraping. Using knowledge from the past scraping lessons this went very smoothy and I was quickly storing them in the way I wanted to. Things were coming together so quickly and before I knew it I was able to search for listings through my CLI interface and dive deeper into the details.

After a little fine tuning I was able to hit my goal of making the menu recursive and made the CLI a bit more visually appealing. I took the extra time to go above and beyond and publish my gem (check it out: "gem install local-real-estate") and am eager to see what challenges face me moving forward.
