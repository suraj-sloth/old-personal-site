---
layout: post
date: 2021-07-26 23:59 +0530
tags: kde dev cpp kmymoney
title: GSoC 2021 KMyMoney - Post First Evals to Week 7
---

# {{page.title}}
<br>

The plan for the post first evals week was to complete the following tasks:

* Make changes as suggested by mentors on my last work.
* Modify the AlkOnlineQuoteSource constructor for new members (m_idSelector and m_idNumber)
* Write unit tests for the added members in the AlkOnlineQuoteSource.

<br>
I modified the code as suggested by my mentors that were related to coding conventions(according to C++, Qt and KDE).

After adding the new members to the AlkOnlineQuoteSource constructor. I jumped into writing the unit tests. I realized that I haven't added the new members in the function signature. After adding that, I build the files to check what all things break related to the constructor's usage. They were :

* defaultQuoteSources() - The function having default quote sources. I modified those according to the new signature with quotes data from webpricequote.
<br>
I proceeded to work on tests then and modified the test functions according to the new signature. I ran all the tests only to realize later that alkonlinequotesourcetest fails. It was due to the undeclared IdSelector variable. After fixing(assigning a default type) it was very relaxing to see all tests pass.

<br>
My work can be found here : [Alkimia](https://invent.kde.org/surajsloth/alkimia/-/tree/gsoc21) and [KMyMoney](https://invent.kde.org/surajsloth/kmymoney/-/tree/gsoc21).

## Learnings - 
I got to know more about the importance of coding conventions and writing tests.

## What's next - 
This week will revolve around implementing the libalkimia changes in kmymoney. I am also looking at this [https://bugs.kde.org/show_bug.cgi?id=439411](https://bugs.kde.org/show_bug.cgi?id=439411) as suggested by Ralf.
<br>
If anyone wants to suggest something or have a discussion please reach out to me on suraj[dot]mahto49[at]gmail[dot]com or @suraj_sloth:kde.org in matrix.
