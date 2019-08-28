# machinelearningstudies
Journal of my Studies in Machine Learning, Fall 2019

## August 27, 2019

I have made two academic achievements thus far, the first is the completion of Andrew Ng's Machine Learning Coursework, and the second is the completion of the OffSec OSCE Hacking Challenge. The following are my reflections thereon. 

Looking back on the OSCE Challenge, it was worth the effort in that it required me to acquire certain skills that weren't part of my a/A education. I'm referring mainly to the skill in understanding assembly language, compiling it, running it, and debugging it. Specifically, the main skill here is inspecting the registers, and the memory to which they point, as the program runs, which is a little bit of a unique task because each register has its own function, and the values are displayed in hexadecimal.  As such, one needs to know both the purpose of each register, and to be able to read hexadecimal fluently.  Once you can do this, debugging assembly feels as natural as debugging a higher level codebase, and it's quite fun. 

It also reminded me of a few interesting things. The first is that programs can be reverse engineered and modified without changing the functionality of the application. This is done using a program that disassembles the executable, and once you have the disassembled program, you can insert new assembly code and then recomplile it. That's pretty cool, and piggy-backing on top of this, one can also pass code around as text in the form of hexadecimal numbers and "disassemble" the text to inspect it. This was the first time thinking about code at this level of abstraction; that is, a much lower level of abstraction than javascript or ruby, and it made be feel powerful.  

Looking back on the past few days, I probably could have been a little bit more systematic about my studies. I spent most of the time jumping back and forth between a few different approaches to running the assembly code, and I may have been better to just decide to figure out how to run the assembly code and debug it with full visibility into the source. It's just that assembly code can be scripted in a several ways (C wrapper, stand alone), and both of them took a while to grasp because the compilation configurations is specific to the machine I'm using, and because the assembly code itself was buggy, or rather, because the code threw an error that I didn't expect, and I had to spend time understanding it. On top of all of this, I had to learn to think in assembly. So I guess i just did all of those things all at once and emerged with some new knowledge. 

If I learn to pen test, I'll take the OCSP course instead. It could be a lot of fun.

-- 

With regard to the Machine Learning Course, there was definitely a lot of material. We covered real world examples for supervised learning (regression and classification), unsupervised learning (clustering and Principle Component Analysis), and then learned how to debug/evaluate ML algorithms using learning curves, error analysis, ceiling analysis, as well as build a few real world ML systems (anomaly detection, recommender systems. Finally, we learned about large scale ML optimizations and how Image OCR uses the sliding window method and system design of ML pipelines. I feel empowered to implement ML systems after doing a course like this. 

That being said, some questions about the fundamentals remain in my mind. I'm specifically curious about the intuition behind certain ideas in linear algebra and statistics. For example, how did somebody come up with singular value decomposition? At this point, all I know is that it's used in PCA, and how to implement it, but I don't really understand how anyone came up with the idea in the first place. I think the problem is that I'm not even clear on more elementary ideas, such as the proof of the equation for the variance of a Gaussian distribution. If I knew it, I would then know that how idea explains the concept of a covariance matrix, of which I also know the equation, but not the intuition. Then, finally, we reach SVD, which is a series of operations on the corvariance matrix. Like I said, I can implement SVD, and the implementation thereof using the 5000-face dataset was nothing short of astounding, and I could follow the code and high level logic, but when I comes to understanding the deep logic, how someone invented it, I'm not following at this moment.

Similarly, I not sure where the intuition arose of the squared length of a vector in n-dimensions being the sum of the values squared. I can see the extrapolation from pythagorean theorum to n-dimensions, but once again, I feel like I'm missing something in my understanding that allowed someone to make that jump and feel justified in doing it. Perhaps it's because I can't visualize greater than three dimensions, and that's all there is to it. 

There are few more things like the proof for K-means clustering, and just how exactly SVMs were conceived, and just generally the awe that people actually invented these tools at all. In a nutshell, I should dive deeper into the minds of the inventors of these algorithms.

-- 

So, thinking back on my original motivation for doing machine learning, I have to ask myself to what extent I have made progress. The intention for this project was to learn exactly what ML can and can't do, and there is definitely some clarity there. 

In some ways, it's quite simple. Every single ML algorithm is simply minimizing of the sum of the errors between hypothesis and actual by using gradient descent or some optimized version thereof to modified parameters of the hypothesis function. The hypothesis function is a linear equation with a possible transformation, and that's really all there is to it. If the algorithm fails, there is a process for examining whether the algorithm has correctly fit the data (is it biased or highly variant?), and whether the performance is adequate (does it have a good F1 score?).  We learn how to perform these evaluations, as well as what to do about it, whether that means changing the parameters of the algorithm, or acquiring more data, or modifying the dataset.

But in reality, ML is not that simple because modeling the real world is complicated. The real world needs to be described with numbers, and the data needs to be collected, and it needs to be normalized (cleaned). This task is so hard that the ML algorithms are only being applied to very concrete problems. Lets take a look at the examples to understand what I mean:

1. Housing prices (linear regression).
2. College acceptance base on two tests (logistic reg.).
3. 0-9 number classification, and streering wheel self-driving care (NN and one-versus-all logistic regression).
4. Image compression (of the color pallete) (K-means and PCA)
5. Anomaly system for computers base on CPU usage and traffic, and airplane motor quality.
6. Recommender system for movies with 100 features.
7. Image OCR walkthrough (NN, logistic regression).
8. Spam Classification (SVM).
9. Face data analysis, PCA 

This is what we worked on, and you'll see that the examples are only problems that can be easily modeled with numbers and for which there is a strong correlation predictable or visible. Housing prices are already numbers, and college acceptance prediction already has numbers with a visible correlation. Number classification is concrete and requires extremely clean data. Image compression used a easily groupable parameter: the color pallate (RGB). The anomaly detection assumes the data is Gaussian. Movie recommendation is discreet (5 levels) and already representable in numbers. Spam is also easily representable with numbers (count the words). This is all to say that the examples were easily representable in numbers - how could you accurately represent difficult ethical problems with numbers, and come up with a dataset that people agree upon? I certainly am not sure how to do that at this time.

That is not to say that the solutions to these problems aren't creative or amazing. I'm truly amazed that people came up with this, and I don't claim to understand all of the algorithms completely, or how they work. In fact it's amazing that people came up with the algorithsm, and that they figured how to represent the data in such a way that the data actually worked with the algorithsm. That being said, it's important to say that I don't believe that ML algorithms think in any way, and none of these examples are matters of life and death. If ML is doing any kind of thinking, it's doing the kind of thinking that labels and groups concrete entities, and nothing more than that. 

## August 28, 2019

It has also been a goal to write about my two years in San Francisco. Well, actually, it was about one year and nine months, with two months in New York, and a month in China. Looking back, I miss SF and everything that came with it, despite having wanted to leave when I was there. In fact, I relished the ideas of traveling to NY and China when those opportunities arose, and took them in stride. Interestingly, I found myself bragging to my peers in those places that I was a resident of San Francisco, proud of the fact that I lived in that city. In reality, I was proud of the fact that I survived in that city at all. So when it comes down to it, I didn't really miss SF, I miss those moments when I connected with people despite the craziness of the town, the amount of connections that I didn't make with people, and why would I? There's too many people in a city to meet, and that's just the way it is. 

So I group my time in SF into two episodes. The first was my time the Mission district, and the second was time in SOMA. In the first episode, I developed some skills and cut my teeth as an engineer. I also made friends and met a lot of new people. Of course, both of these things continued in the second episode, but the focus of the second episode was giving back to a/A as a teacher, sharing tips and tricks that I learned, and helping students as things came up. I met people, but on the professional level, in the student/teacher relationship.  So, both were useful, and a lot of things happened around these experiences that I would want to discuss on the more psychological level.

The first thing I want to discuss is the fact that in SF, and specifically in tech, you can be successful without a college degree. In fact, out of my four closest work colleagues across both jobs, not a single one had a college degree, and we were all making the same amount of money, or they were making more. That was the situation. So, in reality, the idea of getting into tech without a formal background was totally true. Actually, I met, or heard of, a few other people that fit this model. A friend of my colleague, for instance, worked for Facebook from age 16 and worked on React. He didn't go to college. Another once-removed colleague was living in SF after having sold some software to Google for their search team, and made a ton of money on it. And there are more stories like this: Wayne Chang sold Twitter a video streaming feature for 200 million dollars. POF creator, Marcus Find, according highscalability.com, and as of 2010, made 10 million a year from advertising by running his dating site out of his own computer. And lastly, one should know about the 30 million dollar steal that ethereum hackers made from smart contracts that weren't sufficiently protected. In fact, it could have been up to 180 million, but white-hat hackers were able to fix those vulnerable contracts before the hackers could get to them. These are just a few examples that I know...where strong coders had good opportunities and capitalized on them. 

What is moral of this particular story? It's that big money can be made in tech, and this was something worth learning.  As an aspiring engineer, I now have some perspective on what can be done when coding skills can be applied creatively.  I only wonder how much money are in the hands of executives of big tech companies, or even more, the hands of those who controls the manufacturing of the hardware or the infrastructure of the internet, because that hardware is the backbone of the internet. But really, who gets the money? Those who built the microprocessor, or those who built the video streaming feature? Both are necessary, and technically, one depends on the other, and actually, I have no idea how the money distributed among those who get that microprocessor built and installed in a computer. Who even knows everything that's necessary to build a computer from raw materials all the way to a fullying functional machine that interfaces with the internet? Why do I even ask myself these questions? 

To me, it's kind of like the piano in that Beethoven built the piano, not because he literally built it, or even knew how to build it, but because his ideas about music inspired builders to improve the machine with the purpose of giving him a machine that could express his ideas. In the same way, computer builders probably build the machines so that they can express the ideas, or rather, perform the computations necessary for those who are dreaming up new ideas right now. In fact, after having studied machine learning, I think research into quantum computing is fueled now by the potential for it to solve problems that many people want solved in ML, but can't do at this moment. 

I'm speaking specifically of the cost functions that form the foundation for machine learning algorithms. These algorithms try to minimize the cost function through iterative processes like gradient descent. More speciically, they traverse the n-dimensional space that maps the parameters to the cost function. Now, this can take a long time, but with a quantum computer, this particular computation can be done in constant time, and that is amazing. As such, the quantum computer manufacturers and researchers are driving by the idea that this new technology can transform our ability to express new ideas and solve new problems, which I basically just group into the same fundamental thing. 

So once again, those with the ideas hold the most power. That is assuming, however, that they can express them and convince others to organize around them. I guess this is what I learned in SF. 

Another thing I wondered in SF was why the manufacturing of these machines happened half-way around the world. If I work with computers everyday, why can I go to the computer shop across the street from my job and learn something about it. Why can't I open up my computer and learn something about the hardware? How deeply can I even inspect the inner workings of my computer? Do I know what every bit is doing in my machine? The answer, of course, is absolutely not, and even if I did know, what power would that knowledge give me? I have yet to find out, but my intuition is that it would give me something very powerful, even if I can't put it into words. 

Someone said something very interesting to me in SF. They said that being a software engineer requires trusting many levels of abstraction from the hardware all the way up to the level of software that one is writing. This is true because I definitely don't have the mental energy to imagine every single bit of information that goes through my machine when I write something at a very high level, like an api request in the Chrome browser. Yet, at the same time, what proof is there that, should a problem arise with that API request, there isn't some very small problem at the very lowest level that prevents the api request from work? I don't think such a proof exists, and therefore, it behooves the software engineer to know the inner workings of a computer deeply, and I think there is some way to capitalize on that. 

Actually, I can see the importance of deep knowledge in security research. Knowing the assembly language allows one to reverse engineer any application and modify it. I had to do for the OSCE coding challenge, and I'm sure others do it according to their own goals. In fact, I'm rather shocked by how easy it is do certain things that violate people's privacy on the internet. The browser is a powerful thing, and I'm amazed already that my identity hasn't been stolen more times (it's only happened once).

And so getting back to question of manufacturing, there must be people who know the machine so well that they trust the machinery coming out of China. There must be some serious collaboration between companies like Apple, multinationally, to ensure that these machine are built correctly. Who are those people and what are they up to? Why don't I know about those people and their dreams and creations? They are hidden from the news, or from my own sources of information. They maybe sit somehwere in silicon valley, and go to China to make sure that the motherboards are built to spec, and that the CPUs work correctly, and that the machines do everything they want them to do, and for every piece of hardware, engineers are trying to build it better, and lots of people must be working on it because computers have gotten smaller and smaller every year for the entirety of my adult life, and I couldn't tell you anything, really about what's going on outside of a few memory storage models and the logic gates that I read about, and the basics of assembly language. Outside of that, I know the basics of full stack development, and networking, basics of data structures and algorithsm...I feel so ignorant, to be truly honest, when it comes down to it. 

So this was San Francisco. Lots of new people and new ideas. A fresh perspective on the world much bigger than what I imagined, and the opportunity to meet people who have achieved things in this field. I went to San Francisco with the idea that I could be a master of software engineering in three months. That was an absurd idea, but a necessary one that would motivate me to make the move and see what was out there. Ultimately, what I discovered was astounding: that computing machines and the internet were an overwhleming massive operation that spans the entire globe, affects everybody in it on a cultural and political level, and I knew basically nothing about any of it, despite the fact that my interaction with it forms the foundation for how I interact with people around me.

About halfway into my San Fran adventure, I read an article about the city of Baotou, a manufacturing plant in western China that produces Cerium and Neodymium, minerals that are in screens and magnets respectively. According to the article, the place is a toxic waste dump, akin to the industrial landscapes of Detroit during the America's industrial age. Moreover, the cultural landscape in Baotou is fascinating. Regardless of what it is, the city is half way around world, but it produces things that are in this machine that I'm using right now, and because this machine exists, I no longer have to write with my hands. Instead, I can type on this machine, and I can make my thoughts public to basically the entire netizenry with a push of a button. That is an insane amount of power.  




