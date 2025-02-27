---
title: Why writing a small standard library might be a good idea.
date: 09=07-2024
categories: [programming]
tags: [C,programming,42]
---

# Why writing a small standard library might be a good idea.

Why would anyone start with anything but Python? It is used everywhere. Or the 6000th Js framework? Isn't the new kid on the block always the coolest? 
Who in his right mind would start with a language like C, and then go on to make a boring project like an extended standard library? 
This approach bears some rather obvious fruits I argue, and does not have to be hard or boring. 

```c
#include "libft.h"

char	*ft_substr(char const *s, unsigned int start, size_t len)
{
	char	*sub;
	size_t	s_len;
	size_t	i;

	if (!s)
		return (NULL);
	s_len = ft_strlen(s);
	if (start >= s_len)
		return (ft_strdup(""));
	if (len > s_len - start)
		len = s_len - start;
	sub = (char *)malloc(sizeof(char) * (len + 1));
	if (!sub)
		return (NULL);
	i = 0;
	while (i < len)
	{
		sub[i] = s[start + i];
		i++;
	}
	sub[i] = '\0';
	return (sub);
}
```
> Is that even necessary? 

## 1. Why would anybody do that do himself? 

Don't take my words for it listen to what experienced people say: 

> People who started by learning low level programming languages consistently outperform people who start with higher level languages. 
Jonathan Blow

And that makes sense. I can not imagine getting very confused by pointers very much. They are extremely powerful, but had I spend a lot of time feeling the comfort of high-level languages, I imagine I would not even have pulled it off to understand pointers to a minimal degree. 

There is value of doing something hard first, pushing through it and then believing that the path ahead is something that one can undertake. 

## 2. How you can make it easy for yourself? 

I see two things that help anybody pushing through uncomfortable beginnings: 

1. A need. 
If you need a certain thing, just build it. There is a thousand and one ways to learn code. If you don't have an immediate need than make excellence and enjoying hardship your need. 

And a small secret: C is an easy language after the first hurdles being taken. 

Which leads us to the second point...

2. Being good. (or at least better than yesterday)
Usually you do not only good at what you enjoy but also reversely **you enjoy what you are good at**. 

Make some friends and make small competitions. Find a mentor, find a school. There is so many people out there waiting to help you. 

You can transfer their knowledge. What an honor for you and what resourcefulness and respect it is for them. 

### You can do it!!

