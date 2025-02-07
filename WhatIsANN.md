# What is an artificial neural network ?
![img/concepts.png](/img/concepts.png)
![img/concepts2.png](/img/concepts2.png)
![img/concepts3.png](/img/concepts3.png)
![img/concepts4.png](/img/concepts4.png)
![img/concepts5.png](/img/concepts5.png)
![img/concepts6.png](/img/concepts6.png)


Is this an incomprenshible black box? Kind of. It depends. More on this later.

![img/concepts7.png](/img/concepts7.png)


So any student with a weighted combination of hourse slept and hours studied, will fail if that value is below the yellow-dotted line. Of the student is above and to the right of the yellow line, they pass. As you can see it isn't perfect and doesn't capture every data point. The pic is self explantory. Now if this was a statistics or machine learnin course, you would learn that we can solve this problem using, for example, a logistic regression or perhaps a support vector machine. But in DL (Deep Learning), we are going to solve this using artificial neural networks. 

![img/concepts8.png](/img/concepts8.png)

So we might use a graphical representation of the network to indicate that we have two inputs into the networks, that would be the hours slept and hours studied. The extra term, X of 0, is called a bias. and X of 1 and X of 2 are the features and then we compute a linear weighted sum of the input features (x1 and x2) apply a non-linear activation function like a sigmoid and then get our output of the model, y hat our prediction. 

A different example. Lets say our goal is to seperate the yellow from the blue points. Now this is a trickier problem because it's not possible to draw a straight line! IOW: There is no linear solution. Need a non-linear solution. 
![img/concepts9.png](/img/concepts9.png)


This is where deep learning really shines through. Deep learning is amazing at solving complicated problems that require non-linear solutions.
Well, you can imagine that in this case, the separating line is actually a separating circle.
Again, if this were a statistics course, we could still come up with ways to solve this problem,
but you would need to know apriori that the best discriminator would be a circle.

And with deep learning, you don't need to know anything about the nature of the correct solution. The deep learning model will automatically figure out that something like a circle is a good solution.
![img/concepts10.png](/img/concepts10.png)

#### A little about the math

![img/concepts11.png](/img/concepts11.png)
The xs are the data. Now, here I'm only showing two data values, but of course in practice you have lots of data values, maybe dozens or thousands or millions of data values. And these ws here, these are called the weights. These are the numbers that tell the model how important each of these data features is for the prediction, for the model output. Now, we don't actually specify these ws, they are learned by the model through this amazing procedure called back propagation.

So we can think back to our example of passing or failing an exam. Let's imagine that variable x2 was the number of grapefruits that the student ate in December two years ago. Well, you know,
that's a weird variable to include in the model, and it's unlikely to be relevant for predicting whether someone will pass an exam tomorrow. So the deep learning model will learn that this variable is not predictive, and therefore, the model will learn to set this weight value to zero.

Okay, now, this equation here is linear. <font color="lime">It has multiplications and sum, which is the definition of a linear model.</font> So a model that looks like this, that has this equation, can solve linear problems but not non-linear problems. So therefore, **in deep learning, we add a non-linear function to this linear expression.**

So we take the linear part of this equation and we pass it through some non-linear function, which is what this sigma here represents. 
![img/concepts12.png](/img/concepts12.png)

Now, this non-linear function is usually something really simple. <font color="lime">In fact, it turns out Now, this non-linear function is usually something really simple. In fact, it turns out that these simpler, non-linear functions tend to work better than complicated, non-linear functions.</font>

So here I'm showing an example with a log function. This is just an example to make the point more concrete. 

![img/concepts13.png](/img/concepts13.png)

Okay, now this one equation here is neat, but you know, this is not very powerful on its own.
So what we do in deep learning is treat this thing as an elementary building block. It's like a brick. And then we build an entire complicated world class structure by putting a lot of these simple bricks together. And then we can visually represent that using a diagram that would look something like this. 
![img/concepts14.png](/img/concepts14.png)

Now, each of these circles here, each of these units,these are sometimes called artificial neurons, although I actually strongly dislike that term for reasons that I will explain in a later video. But anyway, each of these units actually represents the simple equation that I showed in the previous slide.
![img/concepts15.png](/img/concepts15.png)

 Now, here I'm using a slightly different notation just to make it more compact and also more general but this expression really is just the linear weighted combination plus the non-linearity. And the key is that we repeat this simple computational building block many, many, many times.

Now, obviously there is more to know about deep learning than just this one slide, but this really is the elementary procedure. This really is the idea of deep learning. So in general, the deep learning model is a transformation from some input data into an output prediction about the real world. There are different families or different ways of optimizing deep learning models for different kinds of problems. If you have a data table and you want to predict an outcome, then you're probably going to use an a ANN architecture, like what I illustrated in the previous slide. 

If you have a picture and you want to know whether there is a cat in the picture, then you're gonna use something called CNN or convolutional neural network.

If you have a time series, like an audio clip, and you want to see if you can predict
some specific outcome, then you would use an RNN, which stands for recurrent neural network.

And I already gave another example of translating text from one language into another.
That's also done using an RNN architecture.

So very different kinds of problems and different terms, different model architectures,
but the underlying mathematical and computational principles are all the same.
![img/concepts16.png](/img/concepts16.png)
Furthermore, deep learning models can be visualized in a variety of ways. So different visual representations are used to illustrate the same concepts.

![img/concepts17.png](/img/concepts17.png)


But don't be concerned and don't be intimidated. These different deep learning models are actually all really similar to each other. In fact, they are much more similar than they are distinct so don't be intimidated by the diversity of terms and graphical representations of deep learning architectures. By analogy, here's an analogy, different kinds of buildings may look very different from each other, and different kinds of buildings are suited for different purposes but the electricity, the plumbing, the windows, the ventilation systems,the physics that govern the structural intensity, that's all exactly the same in all these different kinds of buildings.