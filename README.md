      Start your Journey to the Origin of Error! \* { margin:0; padding:0; font-family: 'Noto Sans'; font-size:22px; } h1 { font-size:42px; padding:20px; text-align:center; } h2 { font-size:22px; font-weight:normal; } div { padding-top:22px; padding-bottom:22px; } div.art { width:880px; margin-left:auto; margin-right:auto; } ol > li { padding-top:10px; padding-bottom:10px; list-style:none; } img { padding-top:22px; padding-bottom:22px; } img.img { width:880px; } span.codex { background-color:black; color:white; padding:1px; } pre.codex { background-color:black; padding:42px; color:white; font-family:monospace; margin-top:12px; }

Start your Journey to the Origin of Error with Python!
======================================================

![](images/st1.png)

Hey! You already know something about Python, and most likely you have already written some of your code. Of course, you and Python together are good enough to understand each other from the half-word, and you already had your WOW effect on how close to the natural language Python is, but as a Human being, most likely you already wrote some code that has an Error inside! That is Wonderful. You proved You were a Human.

Are Humans able to produce only Errors?! We are sure that Humans can produce much, much more. And Humans can produce pure code too. If any Error occurs, we are happy since from that point we can get back to the origin of Error with the help of Python and make corresponding corrections, but what is much more important is that we can enrich our internal knowledge and learn something new to change our state.

So what is an Error? We know that there are no Errors for the computer — the computer just executes what is written and tries to do his best. So maybe an Error is just a lack of knowledge when we try to express our dreams in computer form. Or maybe we just have a lack of understanding how to talk to the computer :)

Well. Enough of the philosophy — let's dive deeper!

You write your code. Python tries to execute it, and if he detects some part of your code (or code that you have included inside your source code to use it in your goals) that he cannot execute — he marks this code as an Error. What happens next? At the next step, Python creates an Exception and raises it! And this Exception moves like a comet to the output of your program, moving from one part of the code to another part of the code from bottom to top until someone catches it and processes it. If no part of the code catches the Exception, the Exception moves to the top of your source code and appears inside the output of your application.

The process of showing this Exception (a ghost of the Error) is called tracing. And since we are curious enough, we want to look at the origin of the source, so we trace back to the origin. You can find a lot of similar names for this process: back trace, back react, etc., whatever. Here we talk about Python, so in Python this process is called Traceback (first things first — it is tracing back to the origin).

After this process is complete, we have a side effect: a result that is shown to the user is a backtrack message. And this article is about the format of this message. When we know the form, we can focus our attention on the part of the form we are interested in, here and now.

Hooray for Traceback!
=====================

One moment — it will appear on the scene in a second or two.. Just hold your breath! And here it is:

zkv@moonlight ~/python-projects $ python time.py
What's the time? 12:12
Lunchtime
Traceback (most recent call last):
  File "/home/zkv/python-projects/time.py", line 20, in <module>
    mani()
    ^^^^
NameError: name 'mani' is not defined
zkv@moonlight ~/python-projects $

You can see from the picture above that this message is full of information. Let's look at some parts of the information displayed here:

1.  We can see the concrete name of the Exception that was raised.
    
    NameError
    
2.  We can see the message from the exception; it might help us from time to time :)
    
    name 'mani' is not defined
    
3.  Part of the code without errors
    
    What's the time? 12:12
    Lunchtime
    
4.  We can see the calling stack
    
    Traceback (most recent called last):
      File "/home/zkv/python-projects/time.py", line 20, in <module>
        mani()
        ^^^^
    
5.  Path to the source code of the error (with line number and module name)
    
    File "/home/zkv/python-projects/time.py", line 20, in <module>
    
6.  Concrete error code
    
    mani()
    ^^^^
    

We are sure that this message can be read from top to bottom or from the bottom to the top. Actually, we can display this message any way we want with the help of the traceback standard library module. You can read more about it in our separate article \[link here\].

Here, we want to show you one of the ways to investigate the information from the traceback:

When we see a traceback, we can start asking ourselves questions to be able to move our eyes in the correct direction based on our internal choice. :) Of course, our main question is: why is this message here? We will answer this question ourselves after we complete the investigation. The next question goes to our brain: "What happened? And to this question, we already know the answer. The error was determined, and an Exception was raised. No one caught it, and it stayed unhandled. What type is it? We start to focus deeper — and we investigate the Name of the exception; it points us to the concrete sector of Errors. Maybe this Exception can help us and tell us something. Let's look at the message that was produced by the Exception. No message — no worries — we are smart enough to see the code and make corresponding assumptions. Assumptions that we can and should check. Errors are written in code inside some source file on some line at the position of the cursor; we can find this information from our traceback too. Also, we can find inside which module it happened, and we can actually see the concrete code that leads to the Exception.

But why if the Exception appeared inside the internals as we see it on the screen — it was moving up as a bubble from the deep water from layer to layer from one part of code to another part of code — the same way some time before when the call to the code occurred, but that call was just in another direction? :)

So now we know everything and are free to act. But remember our first question? Why is this mes0sage here? This message is here because we made an Error. So we are Humans. Gratitude to Error! Do we want to correct the Error?! Anyway, we are free and have the knowledge to move forward. Gratitude to the traceback in Python

Oh, by the way… If you run your command with the help of REPL, the result will differ — instead of the names of the source files, you will see <stdin >. Here is a corresponding example:

\>>> def greet( someone ):
>>>
...   print('Hello, ' + someon)
... 
>>> greet("Chad")

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "<stdin>", line 2, in greet
NameError: name 'someon' is not defined

If you do not know what REPL is, no worries — we have already prepared a tasty article about REPL just for you!

Happy New Year, Folks!
======================

P.S.  The first image is generated with the help of MUSE AI.
