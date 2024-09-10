---
layout: default
title: Wired Article: Could the Moon Actually Crash Toward Earth?
parent: Earth Moon
nav_order: 7
---
# Could the Moon Actually Crash Toward Earth - WIRED

# Could the Moon Actually Crash Toward Earth? - WIRED

[Rhett Allain](https://www.wired.com/author/rhett-allain)

[Science](https://www.wired.com/category/science)

09.24.2021 07:00 AM

# Could the Moon Actually Crash Toward Earth?

The trailer for the film *Moonfall* shows our satellite getting too close for comfort. Here are the physics of what it would take to push the moon out of orbit

Photograph: Nasa

![Science_moon_iss064e048655.jpeg](Could%20the%20Moon%20Actually%20Crash%20Toward%20Earth%20-%20WIRED.assets/Science_moon_iss064e048655.jpeg)

There's a trailer out for a new science fiction film called [*Moonfall*](https://www.youtube.com/watch?v=H2jsuTY2uvY), to be released in early 2022, in which the moon is about to crash into Earth. It features several shots of a reddish moon hovering *extremely* close to the planet, crumbling apart while sucking the oceans toward it, the debris flying into spacecraft and mountains. It doesn't actually show a collision—you know, it’s just a trailer and they don’t want to spoil everything.

This isn’t the first movie to stretch the bounds of believable physics. (Remember [*Sharknado*](https://www.wired.com/2014/08/sharknado-2-marketing/)?) But just because it's science fiction doesn't mean it's totally wrong. That's why I'm here: I'm going to go over the actual physics that would apply if the moon ever got too close to us.

How Could the Moon Crash Into Earth?

According to [the movie’s official IMDB entry](https://www.imdb.com/title/tt5834426/plotsummary?ref_=tt_ov_pl), “a mysterious force knocks the moon from its orbit,” precipitating its plunge toward Earth. That’s not a lot to go on. Would there really be a way to make that happen?

Let's start with a basic model of how the planet and its satellite act on each other. A gravitational force pulls Earth and the moon toward each other. This force depends on the mass of both objects and has a magnitude inversely proportional to the square of the distance between the centers of the two bodies.

Here is an expression for just the magnitude of this force. (Really, it's a vector.)

Illustration: Rhett Allain

![Science_emgravity.jpeg](Could%20the%20Moon%20Actually%20Crash%20Toward%20Earth%20-%20WIRED.assets/Science_emgravity.jpeg)

In this expression, *G* is the universal gravitational constant. The masses of the moon and Earth are mm and mE. The distance between them is *r*.

You might think that this gravitational force would be all you need to make the moon slam into the planet—and that would be true if the moon wasn’t in orbit around Earth. However, since the moon is moving in a direction that’s perpendicular to the gravitational force, this force causes its path to curve in one direction so it loops around the planet instead of diving into it.

Forces cause a change in momentum, where momentum is the product of mass and velocity for an object (represented by the symbol *p*). We call this [the momentum principle](https://www.wired.com/story/physics-momentum-principle-work-energy-principle/), and it looks like this:

Illustration: Rhett Allain

![Science_momentumprinciple.jpeg](Could%20the%20Moon%20Actually%20Crash%20Toward%20Earth%20-%20WIRED.assets/Science_momentumprinciple.jpeg)

Since velocity is a vector, the value of momentum depends on the direction the object is moving. If a force pulls on an object in a direction perpendicular to its momentum, that object will move in a circle with the force pointing toward the center. So, the moon moves in a circular orbit because there is a "sideways" force pulling on it due to its gravitational interaction with Earth.

But wait! If Earth pulls on the moon to make it move in a circle, wouldn't the moon pull *back* and make Earth also move in a circle? Yup! Both bodies are interacting and both objects orbit around a common center of mass. You can think of the center of mass as a “balance point” for everyday objects. For the Earth-moon system, this center of mass will be *much* closer to Earth since its mass is so much larger than the moon’s.

Of course, the motion of Earth is much smaller than that of the moon, but here’s why that happens. There's only one gravitational interaction between Earth and the moon—so the magnitude of the force that the moon exerts on Earth is the same as the magnitude of the force that Earth exerts on the moon. Both should have the same change in momentum, since they have the same force.

However, since the mass of Earth is 81 times larger than the mass of the moon, it will have a smaller change in velocity. That means the size of its circular orbit will be much smaller. The orbital radius of Earth is actually smaller than Earth itself, which means that the center of mass of the planet moves in a circle—but that circle is smaller than the planet. In the end, this just looks like a slight wobble.

Now I’m going to use this very basic introduction to orbital mechanics to build a model of the Earth-moon system in Python so that we can see what happens when some mysterious force pushes on the moon. If you want all the details of how to build this model, here's a video:

### Content

You must give consent to targeting tracking to see this content. .

With that, I get the animation below:

Illustration: Rhett Allain

If you think this looks weird, that's because this is the correct Earth-moon distance scale. Many illustrations show both bodies as being much larger so that it looks better. I'm not going to do that because I want to treat you as real humans and not lie to you.

I hope you realize that this is not running at the correct speed. If I did that, it would take 28 days for the moon to make one orbit and that's too boring to watch. Notice that Earth does indeed move around in a circle. If you don't believe me, [here is the code that I used to make that animation](https://trinket.io/glowscript/65a63e4352)—you can check it for yourself.

Now we are ready to mess some stuff up. Let's start by pushing the moon *toward* Earth. I'm going to use a force that's 50 times greater than the gravitational force from Earth, applied for 1 hour. We need a force with a large enough magnitude so that we can see some effect—but the time needs to be short enough that we don't have to worry about changing the direction of the force as the moon moves.

Here's what that looks like. (I put in a big arrow to represent the direction of the "mysterious force.")

Illustration: Rhett Allain

![Science_moonpush1.jpeg](Could%20the%20Moon%20Actually%20Crash%20Toward%20Earth%20-%20WIRED.assets/Science_moonpush1.jpeg)

This simulation runs for about 8 months after that initial one-hour push. Notice that even after all that time, the moon has not crashed into the planet. The push just caused it to shift to an elliptical orbit.

Since the mystery push was pointed through the center of mass of the Earth-moon system, it didn’t change the angular momentum of the system. [Angular momentum](https://www.wired.com/story/what-is-angular-momentum/) is a measure of rotational motion that depends on mass, velocity, and position. The angular momentum of the moon is constant, so as it gets closer to Earth, it has to speed up its orbital motion. However, since it’s moving faster in a sideways motion (orbital motion), this increase in speed makes it just zoom past Earth and miss it all together.

Also, the Earth-moon system is now moving to the left. This is because the push exerted an external force on the whole system such that the total momentum is now to the left. This would cause Earth to change its orbit with respect to the Sun, but the shift would be fairly small, so don't worry about that. Let's worry about that moon.

In fact, let’s try another push. We’ll use the same amount of force for the same one-hour interval, but instead of pushing toward Earth, this one pushes in the opposite direction as the motion of the moon. Here's what happens:

Illustration: Rhett Allain

![Science_moonpush2.jpeg](Could%20the%20Moon%20Actually%20Crash%20Toward%20Earth%20-%20WIRED.assets/Science_moonpush2.jpeg)

With a push in the opposite direction, the angular momentum decreases. This means that the overall rotation rate gets smaller. The moon doesn’t totally stop orbiting, but it is now orbiting slowly enough that it acts more like a rock falling toward Earth and almost hits it.

(Yes, in the illustration it looks like they collide—but remember that I made Earth and the moon bigger than they should be so that you could see them. In reality, it would be more of a near miss.)

The best way to make Earth and the moon crash would be to just completely freeze its orbit, or in physics terms, to decrease the velocity of the moon to zero (with respect to Earth). Once the moon stops orbiting, it would just fall right into the planet, because the gravitational force from Earth will pull on it and cause it to increase in speed as it heads toward the planet. This is essentially the same as dropping a rock on Earth, except that it’s so much bigger that you could make a movie about it.

To accomplish this, you would either need a bigger “mysterious” force or a push for a longer time. (If there are any aliens out there reading this, please don't use this as a blueprint for destroying Earth.)

Could the Moon Pull Away Earth's Oceans?

But a crash isn’t the only way the moon could demolish us. At one point in the trailer, it looks like the moon is so close that its gravitational force pulls the ocean away from the planet’s surface. Could that really happen?

Let's start with the simplest case, where the moon and Earth are stationary and almost touching. It would look like this:

Illustration: Rhett Allain

![Science_closeearthmoon.jpeg](Could%20the%20Moon%20Actually%20Crash%20Toward%20Earth%20-%20WIRED.assets/Science_closeearthmoon.jpeg)

Now suppose I put a 1 kilogram ball of water on the planet’s surface. Since that water has mass, it has a gravitational interaction with Earth, pulling the water toward the center of Earth. But there is also a gravitational force from the moon pulling in the opposite direction. Which force would be larger?

We can calculate both using the same universal gravitational force for the orbit of the moon. For the interaction with Earth, we will use the mass of Earth and the mass of the water. (I picked 1 kg to make it simpler.) The distance (*r*) will be from the center of Earth to the surface—that's just the radius of Earth. For the interaction with the moon, I will use the moon's mass and the radius of the moon (plus a little extra since they aren't quite touching).

Of course, I used Python, which is the best calculator. ([Here is the code](https://trinket.io/glowscript/b590d4054f) in case you want to change anything.) That gives the following output:

Illustration: Rhett Allain

![Science_forcecalc1.jpeg](Could%20the%20Moon%20Actually%20Crash%20Toward%20Earth%20-%20WIRED.assets/Science_forcecalc1.jpeg)

You can see that the gravitational force from Earth is much larger than the force from the moon. If this was a "tug-of-water," the planet would win. The ocean wouldn't leave.

But what if the Earth-moon system isn't stationary, but in a very close orbit both moving on a circular path around a common center of mass?

If the bodies are moving, that means that the water is also moving, since the Earth-moon system will be moving in a circle. In order for the water to stay on Earth, the total force (the sum of the gravitational force from Earth and the moon) would have to be equal to the force needed to move that water in a circle.

Instead of making the water move in a circle, I can instead use the reference frame of Earth and add a centrifugal force. This is a force you need to add to an accelerating reference frame so that normal physics rules work—[here is a more detailed explanation](https://medium.com/swlh/centripetal-vs-centrifugal-forces-whats-the-difference-4b5f848ae9bd).

So, if the moon is super close to Earth and they are in circular orbits around a common center of mass, then they would make a complete orbit in only 2.3 hours (instead of 28 days). This means that that block of water on Earth’s surface facing the moon would have a centrifugal force of 3.55 Newtons pulling it toward the moon. However, you still have the gravitational force from both Earth and the moon pulling it back toward Earth with a total force of 5.48 Newtons. This means that even in this bizarre orbital situation, the water would still be pulled more toward Earth than the moon.

Basically, this is just an extreme version of ocean tides. Tides are caused by a combination of three forces: the gravitational force from Earth, the force from the moon, and a centrifugal force due to Earth's motion as the moon pulls on it. However, different parts of the planet’s surface are at different distances from the moon, and the net forces result in the water bulging in two places—one on the side of the planet near the moon and one on the far side.

In the end, scientifically speaking, having the moon this close would be super bad. Not only would these extreme tidal forces act on the oceans, but on mountains and buildings, possibly causing them to break down. Yes, it would look awesome, but it could kill us all. Let's just leave it for the movies.

More Great WIRED Stories

- 📩 The latest on tech, science, and more: [Get our newsletters](https://www.wired.com/newsletter?sourceCode=BottomStories)!
- The mission to rewrite [Nazi history on Wikipedia](https://www.wired.com/story/one-womans-mission-to-rewrite-nazi-history-wikipedia/?itm_campaign=BottomRelatedStories&itm_content=footer-recirc)
- [*Red Dead Redemption*](https://www.wired.com/story/in-red-dead-redemption-the-wild-west-is-a-refuge/?itm_campaign=BottomRelatedStories&itm_content=footer-recirc)'s Wild West is a refuge
- 6 things you need to do to [prevent getting hacked](https://www.wired.com/story/how-to-prevent-getting-hacked/?itm_campaign=BottomRelatedStories&itm_content=footer-recirc)
- How to turn your favorite [web apps into desktop apps](https://www.wired.com/story/how-to-turn-web-apps-into-desktop-apps-pwa/?itm_campaign=BottomRelatedStories&itm_content=footer-recirc)
- In Kenya, influencers are hired to [spread disinformation](https://www.wired.com/story/opinion-in-kenya-influencers-are-hired-to-spread-disinformation/?itm_campaign=BottomRelatedStories&itm_content=footer-recirc)
- 👁️ Explore AI like never before with [our new database](https://www.wired.com/category/artificial-intelligence/?itm_campaign=BottomRelatedStories&itm_content=footer-recirc)
- 🎮 WIRED Games: Get the latest [tips, reviews, and more](https://www.wired.com/tag/video-games/?itm_campaign=BottomRelatedStories&itm_content=footer-recirc)
- ✨ Optimize your home life with our Gear team’s best picks, from [robot vacuums](https://www.wired.com/gallery/best-robot-vacuums/?itm_campaign=BottomRelatedStories&itm_content=footer-recirc) to [affordable mattresses](https://www.wired.com/gallery/best-mattresses/?itm_campaign=BottomRelatedStories&itm_content=footer-recirc) to [smart speakers](https://www.wired.com/gallery/best-google-speakers-buying-guide/?itm_campaign=BottomRelatedStories&itm_content=footer-recirc)

