# Vector and matrix transpose

- How to interpret and use the transpose operation in Python and Numpy

![concepts34.png](/img/concepts34.png)

The order of the numbers is the same, so we're not really changing the information that's contained inside of this vector. We are only changing the orientation. So column to row.

Now, you can transpose a row vector and that's going to bring us back to our original column vector.

![concepts35.png](/img/concepts35.png)


So double transpose, you get back to the original vector. Same is true for Matrices

![concepts36.png](/img/concepts36.png)


## The Dot Product!

- Various notations for the dot product
- How to comput eht edot product in vectors and matrices
- Why the dot product is so important in human civilization

The dot product or vector dot product is one of the most important operations in all of applied mathematics. And therefore, the dot product is also one of the most important mathematical operations in deep learning. Fortunately, it's a really, really simple procedure. Computing the dot product is very straightforward.

![concepts37.png](/img/concepts37.png)

So you'll sometimes see the dot product written as a.b, where a and b are both vectors.Sometimes you see the dot product written as a, b inside these angle brackets, these wide angle brackets like this.
Sometimes you'll see a transpose b, and this is actually the most common notation of the dot product, so two vectors a and b, and to compute the dot product between these two vectors, you write a transpose b. That's the most common notation.
Here is actually the mathematical definition of the dot product. So we are summing over n elements in vector a and b, and for each corresponding element, we multiply those two elements together, so simple multiplication and then sum over all of those individual multiplications.

Okay, so lemme show you an example to make sure this is very clear. So we wanna compute the dot product between vector v and vector w.

So we element-wise multiply and then sum. So 1 times 2 plus 0 times 8, that term you see here,
plus 2 times -6 plus 5 times 1 plus -2 times 0. 
![concepts38.png](/img/concepts38.png)

And if you go through all of those individual multiplications, and that gives you 2 - 12 + 5, which gives you -5. So the dot product between these two vectors is -5.

Notice that the dot product is a single number. The dot product between two vectors is always going to be a single number, just one number.

**Now the dot product is not defined for any two vectors. It's only defined for two vectors that have the same number of numbers, so the same length or the same dimensionality.**

They have to have the same number of numbers.

And to illustrate that to you, we're gonna try to compute the dot product between this vector v,
which is the same as the previous slide, and this other vector w, which has fewer elements.

So we have a five element vector and a three element vector.

![concepts38.png](/img/concepts38.png)


Now in the beginning, you know, you can proceed with the dot product just fine, but there's no corresponding elements here for the pairwise multiplication.

So you get five times, you know, nothing, you can't put a zero here because adding a zero here
would actually be giving you a different vector, that wouldn't be the same vector as vector w here.
So the conclusion of this slide is that the dot product is defined only between two vectors that have exactly the same number of numbers, the same number of elements in them.

Of course, you could also chop off these final two numbers here. Then you would have v via three element vector like w, and then you could compute the dot product between them. Okay, so this is dot products for matrices.

We can also compute, sorry, I meant to say vectors.

![concepts40.png](/img/concepts40.png)


This is the dot product between vectors. We can also compute the dot product in two dimensions. And this is something that we are going to be doing when we learn about convolution and convolutional neural networks or CNNs.
So the procedure is exactly the same, we just have more numbers to keep track of. So the dot product between this matrix and this matrix is this element times this element, so 0 times 1 plus 3 times 0 plus 2 times 6 and so on
for all nine of these elements that simplifies to these numbers.

And this is actually pretty straightforward to compute now because we get the sixes cancel. And so we end up with a dot product between these two matrices equal to 20. Again, the dot product is a single number. It doesn't matter how big these vectors or matrices are, we still end up with one single number. And a second point of reminder is that the dot product is defined only between two matrices or two vectors that are exactly the same shape.

They have to be the same size. So in this case, three by three. All right, now let's switch to Python. I will show you how to implement the dot product using NumPy and PyTorch.

So here we are in Google Colab. I'm going to import these two libraries, NumPy and Torch.

So now you know how to compute the dot product,**but what does the dot product actually mean?** How do we interpret the dot product? So the interpretation of the dot product is that it's a single number.
So it's one number that reflects the commonalities between two objects.

![concepts41.png](/img/concepts41.png)

These are two mathematical objects. They can be two vectors, two matrices, two tensors or signals or images
or an image and a filter kernel and so on. So it's one number that reflects the commonality between two mathematical objects, two collections of numbers. 

Now if you're coming from a statistics background,
if you've had a statistics course, you might be thinking that this is a description of, for example, a correlation coefficient or covariance coefficient. And in fact, the correlation coefficient is nothing more than the dot product between two variables. And what makes it a correlation coefficient is that it's normalized in a couple ways,I'm not gonna get into that now, but just to say that the correlation is actually just a fancy way of computing the dot product.

In fact, the dot product is the computational backbone for many things that you are familiar with even if the term dot product is new to you. So for statistics, yeah, well, I won't go through all these, but basically anything you see on this list and more is essentially just the dot product plus some, you know, possibly some fancy normalizations.

In this course, you'll see the dot product when we do convolution, matrix multiplication, and when you learn about style transfer, you'll learn about something called the Gram matrix. And that's also essentially just a fancy application of the dot product.

So in this video, you learned about the dot product. Again, it is the element-wise multiplication and sum between two vectors or matrices.

The dot product is always a single number. It reflects a similarity between those two vectors, and it's only defined for vectors that have the same number of elements or matrices or tensors that have exactly the same shape.

![concepts42.png](/img/concepts42.png)


## Matrix multiplication
![concepts43.png](/img/concepts43.png)


Dummy-corresponding
    - 0 or 1 (false or true)
    - Creates a single vector
    - examples: exam (pass/fail), house (sold/not sold), fraud detection (fraud/no fraud)

    