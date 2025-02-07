# Terms and objects in math and computers

- Important terms in linear algebra and data storage
- "Types" of numbers and variable

![concepts26.png](/img/concepts26.png)

So one number all on its own is called a scalar. It's called a scalar because of the geometric interpretation of linear algebra, where individual numbers are used to stretch or shrink a vector. So a single number just on its own, that's called a scalar.

A vector is either a column or a row of numbers. So you can see this is like one physical dimension, the term dimensionality gets a little complicated in linear algebra, but it's one physical dimension because it's just a list of numbers, so we call this a vector. This will be a column vector. We also have row vectors, this is a matrix, but if you would just isolate this first row, you can see this would be a row vector. So a column vector is standing up, a row vector is laying down on its side. So this is a vector.

A matrix is a two-dimensional spreadsheet of numbers. So this is, you can think of numbers arranged in like Excel, in an Excel spreadsheet, for example, that we call a matrix. And anything higher-dimensional we call a tensor.

In data analysis and signal processing, we work with tensors all the time. In physics, they also work with tensors a lot.

Now, images on computers are stored as matrices. So here's an example of a grayscale image, and it's represented as a matrix. So you can see it's a two-dimensional, so two physical dimensions.
So this is a collection of numbers that you could store in an Excel spreadsheet. And the idea of transforming a matrix into an image or representing a matrix as an image is to convert each number, the value of each element in the matrix into some kind of brightness intensity. So here we have small numbers, so they're dark, and then we get to larger numbers, and they are white.

So grayscale is a matrix. And when you get to color images, now we have to start talking about tensors. You can, yeah, I mean, sometimes people also call this a three-dimensional matrix, which is fine, but we'll call it a tensor for this course.

![concepts27.png](/img/concepts27.png)


### Data types
Means something different in data science than in statistics

![concepts28.png](/img/concepts28.png)

![concepts29.png](/img/concepts29.png)


### Converting reality to numbers
![concepts30.png](/img/concepts30.png)
![concepts31.png](/img/concepts31.png)
So representing categorical data on computers goes by one of two methods. In fact, these are really the same method. I mean, these aren't actually different.

The one-hot encoding thing is given this really bizarre, confusing term for some reason.
Something comes up often in deep learning, you will find actually, is that people who develop deep learning tend to come up with new terms for existing concepts. And I don't know why they do that, just to make things more complicated.


Dummy-coding just means to give something a label of zero or one, which usually means false or true.It's basically where you have two possible options and you assign one option to be zero and the other option to be one.

And then we have one-hot encoding, which is basically like dummy-coding, but for multiple categories.

Now, this creates a matrix, and let me actually just show you. I'll give you an example on the next slide and I think that will make things clear.

Okay, so this was an example of dummy-coding.
![concepts32.png](/img/concepts32.png)





And here is an example of one-hot encoding. So let's imagine we have different movies and we have a deep learning model that's trying to predict the genre of the movie based on, I don't know, some reviews or whatever. So in this case, we have three example movies, y1, y2 and y3.
And each of these movies are given a label, a genre label of history, sci-fi, or kids movies.
So now we represent y1. So movie y1 is a sci-fi movie. So it gets a one over here, a zero for history and a zero for kids.

Likewise, movie y2 is a kids movie, so it gets a one for the kids column and zeros for sci-fi and history. And similar for y3.

So you can see that this is actually exactly the same thing as dummy-coding.

The only difference between dummy-coding and one-hot encoding is that with one-hot encoding,
we dummy-code for multiple different features or multiple different categories, and then we combine all of those into a matrix. 

So the matrix representation of this table would simply look like this.
![concepts33.png](/img/concepts33.png)

So each column corresponds to a dummy-coded categorical variable, and each row corresponds to a different observation, or in this example, a different movie. So that was different ways of converting or representing real-world outcomes using numbers.

And the main difference is that dummy-coding is for one feature and one-hot encoding is basically just a collection of dummy-coded variables for multiple features.