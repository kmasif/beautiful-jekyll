---
layout: post
title: How to Ignore logging from An Imported Module in Python

---

`logging` is the best module you can use in your code to log all the information you would need, for example, for debugging purpose. I use it extensively with any tool / program I write in Python. 

The beauty of python is being able to use all those extensive APIs/modules that have already been developed over the years and work like a charm in your own code / program as needed. One nuisence though is some of them uses `logging.StreamHandler` which sometimes overrun your programs console output. 

The quick solution to this nuisance is to disable that undesired logger by the following line of code:

`logging.getLogger(*name_of_the_logger*).disabled = True`

If you are not sure about the name of the logger that you would like to ignore, use the dictionary that contains all the loggers your program creates: `logging.Logger.manager.loggerDict`.