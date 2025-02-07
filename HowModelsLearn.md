# How Models Learn

- A high-level summary into the mechanism of learning in artificaul neural networks (ANN)
- The difference between forward and backwards propagation
- A (kind of silly) analogy for understanding how deep networks learn.

Okay, so let's imagine you are a chef. You are a famous peanut butter and jelly chef at a Michelin star restaurant, one of the top restaurants in the world. And you are the main chef for making peanut butter and jelly sandwiches.

So you want to make the best possible PB&J sandwiches you possibly can, and you want to keep improving your sandwich making skills, and you improve your sandwich making skills by getting feedback from your customers.

So you give your sandwich to a customer  and the customer says, "Well, you know, it's pretty good, but I think it's a little too sweet." So what do you do if the sandwich is too sweet?
Well, you know, you have a couple of options. You can use less jelly or you can use more peanut butter. 

And how do you know which of these two strategies, or maybe both, of course, which of these strategies should you actually take? Well, the solution according to deep learning, is to keep making more and more sandwiches and get more and more feedback until the customer is happy.
So you keep making more sandwiches each time adjusting, systematically adjusting the amount of jelly and the amount of peanut butter. And eventually the customer is gonna be happy and will stop giving you this negative feedback.

So in other words, you use the negative feedback from your customers to adjust your behavior
and you stop adjusting your behavior, and the behavior here is your PB&J making when you get the positive feedback.

Okay, so let's work with this analogy a little bit. So we are going to map this analogy onto the equation of forward propagation that I introduced you to in the previous video.
![concepts18.png](/img/concepts18.png)

So remember that linear equation looked something like this.  So we have the output of the model, and in our analogy that's the sandwich. And then we have the X values that in the previous video I said that the X values correspond to data, and that is true in the real world,
in real deep learning models.

Here in our analogy, we're gonna pretend that these are the ingredients. So X zero aka X naught, is the bread, and there's no weight for that.

So is, you know, we just have two slices of bread. X1 is the peanut butter, and X2 is the jelly.And then we have the Ws here, W1 and W2.

And in the previous video I said, that these Ws are called weights and they encode the importance of each data variable or each data feature.
<font color="lime">
Now, in this analogy, this would correspond to the amounts. So W1 is the amount of peanut butter
that you put in the sandwich, and W2 is the amount of jelly that you include in the sandwich.
So then forward propagation involves taking these raw ingredients, putting them together in exactly the right proportions, and that gives us our output, our sandwich. And then the idea is that through learning, we are slowly adjusting the the W1 and W2, so the amount of peanut butter and the amount of jelly to give us the perfect PB&J sandwich.</font> Now, in the previous video I also showed you a diagram that looks something like this. 
![concepts19.png](/img/concepts19.png)

And I said, that each of these nodes here corresponds to that entire linear equation plus a non-linearity.

So I'm dropping the non-linearity here for, you know, the sake of the analogy and well, hmm, how do we fit that concept, our analogy, our imaginary scenario? How do we map that onto this deep learning model, which has multiple layers?

Well, it doesn't quite fit in. Instead, our model, our equation actually looks a little bit more like this.

![concepts20.png](/img/concepts20.png)

So here we have the three ingredients. This would be the diagram that represents our model, the three ingredients. And **we have the the bread, which doesn't take any weights because you always use two slices of bread and the weight for peanut butter and the weight for jelly.** You combine all of these, you take the weighted combination of these raw ingredients, the raw input data features, you combine them in just the right way and you get the output of the model, which in our case is a sandwich. 

Now what we call forward propagation, where you start from the data,you weight all of the data points, the input data features, and put together the sandwich that is forward propagation.

You start from the left and you move to the right, forward propagation.

And then we have backwards propagation. As I mentioned, it's often called back prop, it's just shortened to back prop. That is the procedure of going backwards based on feedback. So when our customer tells us that the sandwich is too sweet, or you know, it's too whatever, it's too gooey, whatever is their feedback, that error message, that negative feedback gets propagated backwards through the model from the output through all of the nodes into the input.

So, and then the idea is that that error signal is being used to adjust these weight values.
So maybe this weight goes up a little bit and this weight goes down a little bit.

Now you're probably wondering, how do we know whether to increase or decrease these weights? Now that is where we need to get a little bit of math involved. We need to learn a little bit of calculus and a little bit of a procedure called gradient descent and optimization mechanism called gradient descent. 

We will get to the details later. The important concept here is that our negative feedback starts from the output of the model and it gets propagated backwards through the weights and the weights get adjusted. And that is called back propagation.

Okay, so now I'd like to change the analogy a little bit to allow us to think about more complicated models and think a little bit more about forward propagation and back propagation.

So now, instead of just being you the chef on your own, the lonely chef making the PB&J sandwiches all by yourself,instead, let's imagine you run a business.

This is an entire company just for making peanut butter and jelly sandwiches. Now our company has multiple layers in the company.

 We have the raw ingredients, the bread and the jelly, and the peanut butter. We have the kitchen staff. So you know, there's like four people working in the kitchen and they have to take the raw ingredients and put everything together.
 ![concepts21.png](/img/concepts21.png)


But then, you know, this is like such a successful business that we need an entire marketing department to make commercials and advertisements, and to go on Twitter and market our amazing PB&J sandwiches. And they are taking information that's coming out of the kitchen, new ways of making PB&J sandwiches and so on. And then, you know, all this gets fed into the CEO.

Let's say that's you. And then you know, what we predict here is a profit. That's kind of what we want to go for here. Again, not a perfect analogy. Don't think about it too much. This is just something funny and cute to help you get the concept of forward propagation and back propagation.

So forward propagation is that money, and services, labor are flowing through this network
according to these arrows. And they all combine here and they get to the top where we predict our outcome, which is the profit that we will make. 

And then back propagation is the error message that goes from the owner back down through all the departments. 

Now, here is the point that I would like to stress with this new part of this analogy. When the profits are starting to decrease, so the costs are going up and the revenue is coming down, the owner sees that as an error message. The owner says, "Something is wrong, we are not doing the right thing, we're not getting the correct output or the desired output." 

Now the owner doesn't really know everything about the marketing department. The owner doesn't know about, you know, all the stuff that goes on in the kitchen, all the details that happen in the kitchen. And the owner doesn't need to know that. All the owner needs to do, is that there is a mismatch between how much profit was expected and how much profit was actually earned.

So then the owner says, "Hey, let's have a meeting with the marketing team." And the owner says to the marketing team, "Hey guys, I don't know what you're doing, but you're doing something wrong. You have to fix something and I can't tell you what you have to do because I don't know, I just know that something is wrong." And then the marketing department can look internally and they can say, okay, what are we doing wrong and what can we change based on the owner's feedback?

While the marketing team is saying, "Okay, you know, there's some things that we can change.
We can change a couple things, but you know, we're also just taking what we can from the kitchen."

So then the marketing team has to have a meeting with the kitchen team, and the marketing team says, you know, basically the same thing. This stuff rolls downhill, right? So the marketing team says, "Hey, kitchen crew, we don't know what you're doing.

We don't know exactly what goes on in the kitchen, but something is not right. So figure out what's going wrong and make some improvements."

And the kitchen team says, "Okay, okay, we can, we can work through things. We know what we're doing over here so we can make things better.

The important concept here is that we get one error message all the way at the top to the owner.
The owner tells these guys, do something to make things better. These guys say, tell the kitchen crew to do something better, make a change, do something better, and so on.

You can even imagine more layers in here. Maybe you know, there's some other department that's actually selecting the different features of the data, which means the different ingredients.
So they're gonna start using blueberry jelly instead of strawberry jelly or something like that.

Okay, again, kind of a silly analogy, but the most important concepts from this video are that forward propagation is the flow of information from the inputs, from the data through all of these different layers or different departments. And it's flowing in one direction, which is this direction. And then we have back propagation or back prop, and that is taking one single value of negative feedback.

So something is wrong, and that message, that error message that something is wrong, goes backwards. It flows backwards throughout the model, all the way back down to the beginning.

And the specific instructions, the specific ways that the model gets updated. The way that these weights are changing is unique to every individual node and every individual layer.
So that was another piece of the high level summary of the mechanisms of deep learning models.

And in particular, you learned about forward propagation and back propagation.

