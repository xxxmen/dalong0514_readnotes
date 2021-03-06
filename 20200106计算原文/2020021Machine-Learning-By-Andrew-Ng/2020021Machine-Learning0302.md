# 0302Gradient Descent Intuition

In the previous video, we gave a mathematical definition of gradient descent. Let's delve deeper and in this video get better intuition about what the algorithm is doing and why the steps of the gradient descent algorithm might make sense.
Play video starting at ::15 and follow transcript0:15
Here's a gradient descent algorithm that we saw last time and just to remind you this parameter, or this term alpha is called the learning rate. And it controls how big a step we take when updating my parameter theory j.
Play video starting at ::31 and follow transcript0:31
And this second term here is the derivative term
Play video starting at ::39 and follow transcript0:39
And what I wanna do in this video is give you that intuition about what each of these two terms is doing and why when put together, this entire update makes sense. In order to convey these intuitions, what I want to do is use a slightly simpler example, where we want to minimize the function of just one parameter. So say we have a cost function, j of just one parameter, theta one, like we did a few videos back, where theta one is a real number. So we can have one d plots, which are a little bit simpler to look at. Let's try to understand what gradient decent would do on this function.
Play video starting at :1:20 and follow transcript1:20
So let's say, here's my function, J of theta 1. And so that's mine. And where theta 1 is a real number.
Play video starting at :1:32 and follow transcript1:32
All right? Now, let's have in this slide its grade in descent with theta one at this location. So imagine that we start off at that point on my function.
Play video starting at :1:44 and follow transcript1:44
What grade in descent would do is it will update.
Play video starting at :1:49 and follow transcript1:49
Theta one gets updated as theta one minus alpha times d d theta one J of theta one, right? And as an aside, this derivative term, right, if you're wondering why I changed the notation from these partial derivative symbols. If you don't know what the difference is between these partial derivative symbols and the dd theta, don't worry about it. Technically in mathematics you call this a partial derivative and call this a derivative, depending on the number of parameters in the function J. But that's a mathematical technicality. And so for the purpose of this lecture, think of these partial symbols and d, d theta 1, as exactly the same thing. And don't worry about what the real difference is. I'm gonna try to use the mathematically precise notation, but for our purposes these two notations are really the same thing. And so let's see what this equation will do. So we're going to compute this derivative, not sure if you've seen derivatives in calculus before, but what the derivative at this point does, is basically saying, now let's take the tangent to that point, like that straight line, that red line, is just touching this function, and let's look at the slope of this red line. That's what the derivative is, it's saying what's the slope of the line that is just tangent to the function. Okay, the slope of a line is just this height divided by this horizontal thing. Now, this line has a positive slope, so it has a positive derivative. And so my update to theta is going to be theta 1, it gets updated as theta 1, minus alpha times some positive number.
Play video starting at :3:39 and follow transcript3:39
Okay. Alpha the the learning, is always a positive number. And, so we're going to take theta one is updated as theta one minus something. So I'm gonna end up moving theta one to the left. I'm gonna decrease theta one, and we can see this is the right thing to do cuz I actually wanna head in this direction. You know, to get me closer to the minimum over there.
Play video starting at :4: and follow transcript4:00
So, gradient descent so far says we're going the right thing. Let's look at another example. So let's take my same function J, let's try to draw from the same function, J of theta 1. And now, let's say I had to say initialize my parameter over there on the left. So theta 1 is here. I glare at that point on the surface.
Play video starting at :4:20 and follow transcript4:20
Now my derivative term DV theta one J of theta one when you value into that this point, we're gonna look at right the slope of that line, so this derivative term is a slope of this line. But this line is slanting down, so this line has negative slope.
Play video starting at :4:41 and follow transcript4:41
Right. Or alternatively, I say that this function has negative derivative, just means negative slope at that point. So this is less than equals to 0, so when I update theta, I'm gonna have theta. Just update this theta of minus alpha times a negative number.
Play video starting at :5:2 and follow transcript5:02
And so I have theta 1 minus a negative number which means I'm actually going to increase theta, because it's minus of a negative number, means I'm adding something to theta. And what that means is that I'm going to end up increasing theta until it's not here, and increase theta wish again seems like the thing I wanted to do to try to get me closer to the minimum.
Play video starting at :5:26 and follow transcript5:26
So this whole theory of intuition behind what a derivative is doing, let's take a look at the rate term alpha and see what that's doing.
Play video starting at :5:38 and follow transcript5:38
So here's my gradient descent update mural, that's this equation.
Play video starting at :5:43 and follow transcript5:43
And let's look at what could happen if alpha is either too small or if alpha is too large. So this first example, what happens if alpha is too small? So here's my function J, J of theta. Let's all start here. If alpha is too small, then what I'm gonna do is gonna multiply my update by some small number, so end up taking a baby step like that. Okay, so this one step. Then from this new point, I'm gonna have to take another step. But if alpha's too small, I take another little baby step. And so if my learning rate is too small I'm gonna end up taking these tiny tiny baby steps as you try to get to the minimum. And I'm gonna need a lot of steps to get to the minimum and so if alpha is too small gradient descent can be slow because it's gonna take these tiny tiny baby steps and so it's gonna need a lot of steps before it gets anywhere close to the global minimum.
Play video starting at :6:46 and follow transcript6:46
Now how about if our alpha is too large? So, here's my function Jf filter, turns out that alpha's too large, then gradient descent can overshoot the minimum and may even fail to convert or even divert, so here's what I mean. Let's say it's all our data there, it's actually close to minimum. So the derivative points to the right, but if alpha is too big, I want to take a huge step. Remember, take a huge step like that. So it ends up taking a huge step, and now my cost functions have strong roots. Cuz it starts off with this value, and now, my values are strong in verse. Now my derivative points to the left, it says I should decrease data. But if my learning is too big, I may take a huge step going from here all the way to out there. So we end up being over there, right? And if my is too big, we can take another huge step on the next elevation and kind of overshoot and overshoot and so on, until you already notice I'm actually getting further and further away from the minimum. So if alpha is to large, it can fail to converge or even diverge. Now, I have another question for you. So this a tricky one and when I was first learning this stuff it actually took me a long time to figure this out. What if your parameter theta 1 is already at a local minimum, what do you think one step of gradient descent will do?
Play video starting at :8:6 and follow transcript8:06
So let's suppose you initialize theta 1 at a local minimum. So, suppose this is your initial value of theta 1 over here and is already at a local optimum or the local minimum.
Play video starting at :8:19 and follow transcript8:19
It turns out the local optimum, your derivative will be equal to zero. So for that slope, that tangent point, so the slope of this line will be equal to zero and thus this derivative term is equal to zero. And so your gradient descent update, you have theta one cuz I updated this theta one minus alpha times zero. And so what this means is that if you're already at the local optimum it leaves theta 1 unchanged cause its updates as theta 1 equals theta 1. So if your parameters are already at a local minimum one step with gradient descent does absolutely nothing it doesn't your parameter which is what you want because it keeps your solution at the local optimum.
Play video starting at :9:5 and follow transcript9:05
This also explains why gradient descent can converse the local minimum even with the learning rate alpha fixed. Here's what I mean by that let's look in the example. So here's a cost function J of theta that maybe I want to minimize and let's say I initialize my algorithm, my gradient descent algorithm, out there at that magenta point. If I take one step in gradient descent, maybe it will take me to that point, because my derivative's pretty steep out there. Right? Now, I'm at this green point, and if I take another step in gradient descent, you notice that my derivative, meaning the slope, is less steep at the green point than compared to at the magenta point out there. Because as I approach the minimum, my derivative gets closer and closer to zero, as I approach the minimum. So after one step of descent, my new derivative is a little bit smaller. So I wanna take another step in the gradient descent. I will naturally take a somewhat smaller step from this green point right there from the magenta point. Now with a new point, a red point, and I'm even closer to global minimum so the derivative here will be even smaller than it was at the green point. So I'm gonna another step in the gradient descent.
Play video starting at :10:22 and follow transcript10:22
Now, my derivative term is even smaller and so the magnitude of the update to theta one is even smaller, so take a small step like so. And as gradient descent runs, you will automatically take smaller and smaller steps.
Play video starting at :10:41 and follow transcript10:41
Until eventually you're taking very small steps, you know, and you finally converge to the to the local minimum.
Play video starting at :10:50 and follow transcript10:50
So just to recap, in gradient descent as we approach a local minimum, gradient descent will automatically take smaller steps. And that's because as we approach the local minimum, by definition the local minimum is when the derivative is equal to zero. As we approach local minimum, this derivative term will automatically get smaller, and so gradient descent will automatically take smaller steps. This is what so no need to decrease alpha or the time.
Play video starting at :11:22 and follow transcript11:22
So that's the gradient descent algorithm and you can use it to try to minimize any cost function J, not the cost function J that we defined for linear regression. In the next video, we're going to take the function J and set that back to be exactly linear regression's cost function, the square cost function that we came up with earlier. And taking gradient descent and this great cause function and putting them together. That will give us our first learning algorithm, that'll give us a linear regression algorithm.

## Reading

Gradient Descent Intuition
In this video we explored the scenario where we used one parameter \theta_1?? 
1
???	
  and plotted its cost function to implement a gradient descent. Our formula for a single parameter was : 

Repeat until convergence:

\theta_1:=\theta_1-\alpha \frac{d}{d\theta_1} J(\theta_1)?? 
1
???	
 :=?? 
1
???	
 ????? 
d?? 
1
???	
 
d
???	
 J(?? 
1
???	
 )
Regardless of the slope's sign for \frac{d}{d\theta_1} J(\theta_1) 
d?? 
1
???	
 
d
???	
 J(?? 
1
???	
 ), \theta_1?? 
1
???	
  eventually converges to its minimum value. The following graph shows that when the slope is negative, the value of \theta_1?? 
1
???	
  increases and when it is positive, the value of \theta_1?? 
1
???	
  decreases.


On a side note, we should adjust our parameter \alpha?? to ensure that the gradient descent algorithm converges in a reasonable time. Failure to converge or too much time to obtain the minimum value imply that our step size is wrong.


How does gradient descent converge with a fixed step size \alpha???
 The intuition behind the convergence is that \frac{d}{d\theta_1} J(\theta_1) 
d?? 
1
???	
 
d
???	
 J(?? 
1
???	
 ) approaches 0 as we approach the bottom of our convex function. At the minimum, the derivative will always be 0 and thus we get: 

