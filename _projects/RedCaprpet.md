---
title: "RedCarpet for iOS"
tagline: "An app for students to avail credit from RedCarpet"
website: "https://www.redcarpetup.com/"
skills: ["iOS", "Swift"]
---

During summer last year, I interned with a YCombinator(2015) and Google Launchpad(2016) startup - RedCarpet. So 
basically RedCapet offers credit to students for their personal needs such as mobile recharges, movie tickets, food, 
online shopping, etc. Now, this is a big deal in India as students have zero access to credit from banks - no personal 
credit cards/loans and there are no credit scores for the majority of the population as India is a cash-intensive 
economy.

Here I was tasked with building an iOS app for the same. And oh boy, it was pretty challenging. Every other day I 
stumbled across a fairly complex problem. 

I built the app which has a chat which is backed by a resilient task queue 
which managed the sending and recieving of messages and uploading of other media to servers in a fail-proof way - 
basically anything that required a network connection, was done via this queue. The chat supports, along with plain 
text messages, media which includes - photos, videos, location, etc. Another interesting feautre to note was the inline 
forms in the chat message bubble. Other than the chat, it also had a trivial registration, profile, referral mechanism, 
analytics and the other usual stuff.
