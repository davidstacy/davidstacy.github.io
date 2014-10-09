---
layout: article
permalink: /battling-opsworks
title: "One Brick Wall After Another"
image:
  teaser: brickwall-400x250.jpg
---

We are currently setting up a node.js server to capture some data.  You would think this would be easy, but this is IT, and Cloud, and we want to do it all dev-opsy, so it gets complicated very fast.

In the current process, I am learning at least three different technologies, I have faint acquaintance with at this level, so this makes it even more challenging.  So we have.

- Opsworks platform by AWS.  I am somewhat impressed with this product, slick interface, hiding gory chef details underneath.

- Node.js language/platform.  Very cool, very slick I like this product for this sort of tasks, but it's still new to me.  Oh and of course it has its own package management system... of course.

- Javascript, underlying node.  nice language, but somewhat new to me, although simple enough and I have or should have some familiarity with it.

- Chef, underlying Opsworks, I have familiarity with this, but must learn the Opsworks implementation.

- And last but certainly not least, Amazon Redshift, with which we intend to store a lot of data.

- Add in the fun in stitching all of this together with networking and security and you have a real project.

Progress is being made, we are currently on the 10th deploy, but are still having issues showing winston logs (a node.js logging package), this is probably something stupid simple having to do with a chef/aws interaction, and I'll figure it out later.

The next to last hurdle was a security problem in the way I deployed the redshift DB.
