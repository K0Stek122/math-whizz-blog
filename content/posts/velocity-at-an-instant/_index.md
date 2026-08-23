+++
date = '2026-08-28T16:50:58+01:00'
draft = false
title = 'Velocity at an Instant'
+++
To understand instantaneous velocity have a look at [this desmos graph](https://www.desmos.com/calculator/aja9rx9gg0). Firstly let's define what velocity is, have a go at this yourself.

<!--more-->

{{< discussion-question answer="There's a genuine paradox here: at a single instant, there's no elapsed time and no distance travelled, so the usual \"distance ÷ time\" recipe gives 0/0. The resolution (which the rest of the page builds toward) is that we don't measure it directly — we approximate it by looking at two points that are very close together in time, then imagine squeezing that gap down toward zero. Instantaneous velocity is the value that average velocity approaches as the time interval shrinks to nothing." >}}
Before we define it formally — what do you think "velocity at an instant" even means? If velocity normally needs _two_ points in time to measure a change, how could you talk about a velocity at just _one_ moment?
{{< /discussion-question >}}

Thus given this definition, take a look at the second line on that desmos graph. The line that connects two points — it's different to the tangent line, right!

Let's think firstly about how we could calculate the average velocity here. Let's say position is given by $x(t) = t^2$, and we pick two points on the graph: $t_1 = 2$ and $t_2 = 5$.

$$x(2) = 2^2 = 4$$
$$x(5) = 5^2 = 25$$

The average velocity between these two points is just the change in position over the change in time:

$$v_{avg} = \frac{x_2 - x_1}{t_2 - t_1} = \frac{25 - 4}{5 - 2} = \frac{21}{3} = 7 \text{ m/s}$$

This is exactly what that second line on the desmos graph is showing you — the slope of the straight line connecting the two points $(2, 4)$ and $(5, 25)$. Nothing more than "rise over run".

How is instantaneous velocity different? Instantaneous velocity is calculated from a certain point in time between two points. The length between the two points is arbitrary. Here's the problem with this — let's remember the formula for average time:

$$v = \frac{\Delta x}{\Delta t} = \frac{x_2 - x_1}{t_2 - t_1}$$

Any small non-zero delta will give us an approximation of the instantaneous velocity rather than an accurate value.

Let's say position $x(t) = t^2$, we want instantaneous velocity at $t = 3$

**Δt = 1 (from 3 to 4):**  
x(3) = 9  
x(4) = 16  
Δx = 16 − 9 = 7.  
Average velocity = 7/1 = 7 m/s.

**Δt = 0.1 (from 3.0 to 3.1):**  
x(3) = 9  
x(3.1) = 9.61  
Δx = 9.61 − 9 = .61  
average velocity = .61 ÷ 0.1 = 6.1 m/s

**Δt = 0.01 (from 3.0 to 3.01):**  
x(3) = 9  
x(3.01) = 9.0601  
Δx = 9.0601 − 9 = 0.0601  
average velocity = .0601 ÷ 0.01 = 6.01 m/s

Value seems to be approaching 6. The question to ask here is whether these values are precise or approximations?

{{< discussion-question answer="The average velocity values (7, 6.1, 6.01, ...) approach **6 m/s** as Δt gets smaller and smaller. Each individual calculation above is only an estimate of the instantaneous velocity, not a precise measurement — it's the average velocity over some small-but-nonzero interval, not the velocity at the single instant t = 3. No matter how small you make Δt (as long as it's not exactly zero), you're still measuring a change over a stretch of time, so there's always some rate-of-change smearing happening over that interval. The precise value only comes from asking what the average velocity approaches as Δt shrinks all the way to zero — that's the limit, and it's what instantaneous velocity actually means. In this case, $v(3) = \\lim_{\\Delta t \\to 0} \\frac{(3+\\Delta t)^2 - 3^2}{\\Delta t} = 6$ m/s (exactly). So: the individual rows in the table are approximations, but the number they're converging to (6) is the precise instantaneous velocity." >}}
What number does the value approach here? Furthermore, is the equation above an estimate or a precise measurement?
{{< /discussion-question >}}

## Summary
We had a good look at instantenous velocity. We now understand the need for taking the delta of a period of time in order to get instantenous velocity, and more importantly: we understand _why_ this is an exact instantenous velocity rather than an approximation of it.
