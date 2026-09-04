+++
date = '2026-09-03T12:00:00+01:00'
draft = false
title = 'The Unit Circle'
toc = true
+++
Unit circles by themselves are not crucial for calculus. The reason why we discuss them here is that they are the perfect bridge between traditional trigonometry and the abstract nature of calculus.

<!--more-->

## Radians

To first understand where we are getting at we need to discuss radians. In more advanced math, instead of measuring angles in arbitrary units like degrees — where 360 slices per rotation is just a convention, not something derived from the circle itself — we instead measure an angle by arc length, a value that comes directly from the circle's own geometry.

Let's take a look at the circle circumference formula: $2\pi r$. In a unit circle, that is a circle with a radius of one, the circumference of this circle evaluates to $2\pi \times 1 = 2\pi$. No matter the radius of the circle, the circumference at its core will always contain the algebraic term $2\pi$. A full rotation around the circle — a point traveling all the way around the circumference back to where it started — corresponds to an angle of $2\pi$ radians.

To put it bluntly, $2\pi = 360°$, $\pi = 180°$, $\frac{\pi}{2} = 90°$, $\frac{\pi}{4} = 45°$. You can get the circle's relative rotation from this alone. Any slice of the circle you want.

Notice also that whenever we calculate degrees we always tack on the ° sign at the end to signify they are degrees. Not here. We define radians as $\frac{\text{arc length}}{\text{radius}}$. Let's say the arc length = 5 meters and the radius = 5 meters. From basic unit conversion we know that meters/meters naturally cancel out. Thus radians have no units. This is the beauty of radians. They are relative to the circle and thus they are universal no matter what circle you have.

## The Unit Circle

This brings us to the question: what limitation does the unit circle overcome?

In basic trigonometry, we remember SOHCAHTOA, the mnemonic for remembering how to calculate lengths and angles in right angled triangles. We know from geometry as well that the maximum angle in a right angled triangle is $90°$, and the angles add up to $180°$. What if we want to go beyond that? The unit circle allows us to go further. Take a look at the [Desmos graph](https://www.desmos.com/calculator/qf1mfgt42b). As the $\theta$ (angle of rotation on the unit circle) increases, so does the radian measure of that rotation — all the way up to $2\pi$ at a full lap. What does change direction is the point's position: past $180°$ (i.e. $\pi$ radians), the point has reached the leftmost side of the circle, $(-1, 0)$, and starts heading back toward its starting point along the bottom half, arriving back at $(1, 0)$ when $\theta = 2\pi$.

{{< discussion-question answer="Sine and cosine. Track the y-coordinate of the point as $\theta$ increases and you get the sine curve — rising from 0 to 1 by $90°$, falling back through 0 by $180°$, bottoming out at -1 by $270°$, climbing back to 0 by $360°$. Track the x-coordinate instead and you get the cosine curve, doing the same dance a quarter-cycle out of phase. The unit circle isn't just related to sine and cosine — it's where they live." >}}
What curves does this rotation resemble?
{{< /discussion-question >}}

As $\theta$ increases from 0 to 360, it goes back to the same place. At $\theta = 0$, $\sin\theta = 0$ and $\cos\theta = 1$, thus the point on the circle that we move along with is $(1, 0)$, i.e. one point to the right, zero points up/down. Notice how cleanly sine and cosine curves define this point. The point on the unit circle will always be defined as coordinates $(\cos\theta, \sin\theta)$. From this we get:

- At $\theta = 0$, $(1, 0)$
- At $\theta = 90$, $(0, 1)$
- At $\theta = 180$, $(-1, 0)$
- At $\theta = 270$, $(0, -1)$
- At $\theta = 360$, $(1, 0)$ again

Any angle between those four cardinal points has a cosine and sine value in between too — both always land somewhere between -1 and 1, tracing the point smoothly around the circle rather than jumping between it. And from this we can derive the fundamental sine limit:

$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$

$\frac{\sin x}{x}$ is always "stuck" between $\cos x$ and 1. Because as $x$ approaches 0, both $\cos x$ and 1 approach the same value: 1. Therefore, since $\frac{\sin x}{x}$ is trapped between two functions approaching 1, it is inevitable that $\frac{\sin x}{x}$ also converges to 1.

This can be written cleanly only in radians. If we used degrees, we get:

$$x° = x \cdot \frac{\pi}{180}$$

therefore:

$$\lim_{x \to 0} \frac{\sin\left(x \cdot \frac{\pi}{180}\right)}{x} \approx 0.0175$$

which shows that degrees don't give you a clean constant of 1 to work with — you're stuck carrying that 0.0175 conversion factor instead. This is also how engineers convert degrees to radians, by multiplying degrees by 0.0175. If we used degrees everywhere we'd have to constantly carry that ugly constant with us.

## Conclusion
We had a good look at basic trigonometry required for calculus. We analysed why sines and cosines fit so well into Calculus, and hopefully you now have a better understanding of trigonometry that we will later use for complex calculus complex.
