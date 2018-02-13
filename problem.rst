The Problem
===========

In Tim Berners-Lee's original vision of the World Wide Web anyone could publish a document and anyone could read any document. In fact, the `original WWW software <https://en.wikipedia.org/wiki/WorldWideWeb>`_ was both a web browser and an editor.

Anyone could spin-up a server to publish and anyone with an Internet connection could connect to any server, i.e. it was decentralized.

Over the years this paradigm has gradually been eroded with publishing platforms such as Facebook, Twitter, Medium, Reddit, Instagram, YouTube, etc becoming popular. These are highly controlled platforms where the user can become disempowered without any right of recourse. Of course users can still publish on their own servers, but in many ways these platforms offer a lot of advantages over hosting your own website.

Centralized platforms are preventing communities from flourishing in a way that would otherwise be possible.

Advantages of current centralized solutions
``````````````````

Social graph
------------
Most successful publishing platforms rely on some form of social organization - and this has been key to their success. On Facebook you can add your friends that you want in your network. On Twitter and Medium you can follow those whose opinions you want to hear. On YouTube you follow your favorite channels.

Voting
------
Liking, voting up/down, etc has become so vital to the content ecosystem. The open web has never really had this soft of functionality become popular.

Moderation
----------
Reddit and Facebook groups have become very successful in part becuase of their moderation systems. The open web doesn't have a moderation system, although Google has been filling this role to an extent.

Machine readable data
---------------------
Originally, web pages were whole documents and CSS was used to for styling. Of course this was completely inadequate. Developers started to put design into HTML and dynamically generating web pages on the backend. This makes it very difficult for a machine to parse the information. In recent years the Semantic Web has been used to re-add the actual machine readable information into web pages.

Content needs to machine readable first. Templating and styling are presentation layer and should be implemented on the front-end. Facebook and Google maps are much better than the open web at publishing information because they are machine-readable first.


Disadvantages of current centralized solutions
``````````````````````

Hard censorship
---------------
Twitter sometimes bans people entirely.

* `Ahed Tamimi <https://www.rt.com/usa/414396-twitter-delete-ahed-tamimi/>`_
* `Milo <https://www.buzzfeed.com/charliewarzel/twitter-just-permanently-suspended-conservative-writer-milo>`_

On Medium content creators are sometimes `ordered <https://medium.com/@nuckable/the-post-stays-up-except-when-it-criticizes-another-company-our-founder-has-helped-create-9c524abe011e>`_ to change their content under threat of it being removed altogether.

Large sections of Reddit will sometimes `disappear <https://www.youtube.com/watch?v=ub0JDnaU9UA>`_.

Shadow banning
--------------
Both Twitter and Reddit will block users in such a way that it will not be obvious to the user
https://www.youtube.com/watch?v=64gTjdUrDFQ

India's subreddit
https://medium.com/@krantikaari_r/how-indias-biggest-sub-reddit-is-being-silently-censored-16ac656624e6

The ability to publish should be an unaliable right - no should be able to take it away from you.

Platform operators can change anything
-----------------------
Because centralized platforms have operators, they have the power to change anything. For example the CEO of Reddit once `edited <https://www.theverge.com/2016/11/23/13739026/reddit-ceo-steve-huffman-edit-comments>`_ comments that critized him.

Moderator powers
----------------
On Reddit the content locked into a specific sub-reddit can have a moderator team with an agenda and powers to enact it:

* deletion of comments & hiding the deletion with CSS
* deletion of posts
* deletion of posts about deletion of posts
* deletion of posts about requesting removal of mods (censoring community desire for new filter bubble)
* opportunist adjustment of comment ordering
* shadowbanning
* 30/7-day bans

A good example of this is what happened on r/Bitcoin: https://medium.com/@johnblocke/a-brief-and-incomplete-history-of-censorship-in-r-bitcoin-c85a290fe43

Lack of history
---------------
On Reddit, you see content from subreddits you are subscribed to. Typically ordered by an opaque algorithm called “hot”. Users can vote, but there is no real way to see how this affects what content is displayed. Large sections of the site will sometimes disappear.

Content is locked into the platform
--------------------
Each of these platforms works in a certain way and has a legal entity that has control over the platform. If a developer wishes to innovate and change how a platform works they need to create an entirely new platform with new content. APIs are available to interact with the existing solutions, but these tend to be limited in scope and do not alow the fundamentals how how a platform operates to be changed.

User tracking
--------

Some platforms, like Facebook, only allow content to be viewed when logged in. This makes it extremely difficult to browse with anonimity.
