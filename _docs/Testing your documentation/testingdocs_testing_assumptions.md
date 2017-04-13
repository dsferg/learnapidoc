---
title: "Testing documentation assumptions"
course: "Documenting REST APIs"
permalink: /testingdocs_testing_assumptions.html
weight: 2
sidebar: docapis
section: testingdocs
---

While testing your documentation, you must recognize that what may seem clear to you may be confusing to another, because all documentation builds on assumptions that may or may not be shared with your audience.

{% if site.target == "web" %}
* TOC
{:toc}
{% endif %}

## Assumptions in developer docs

You may assume that users already know how to SSH onto a server, create authorizations in REST headers, use cURL to submit calls, and so on.

Usually documentation doesn't hold a user's hand from beginning to end, but rather jumps into a specific task that depends on concepts and techniques that you assume the user already knows.

Making assumptions about concepts and techniques your audience knows can be dangerous. These assumptions are exactly why so many people get frustrated by instructions and throw them in the trash.

For example, my 10-year-old daughter is starting to cook. She feels confident that if the instructions are clear, she can follow almost anything (assuming we have the ingredients to make it). However, she says sometimes the instructions tell her to do something that she doesn't know how to do &mdash; such as sauté something.

To *sauté* an onion, you cook onions in butter until they turn soft and translucent. To *julienne* a carrot, you cut them in the shape of little fingers. To *grease* a pan, you spray it with Pam or smear it with butter. To add an egg *white* only, you use the shell to separate out the yolk. To *dice* a pepper, you chop it into little tiny pieces.

The terms can all be confusing if you haven't done much cooking. Sometimes you must *knead* bread, or *cut* butter, or *fold in* flour, or add a *pinch* of salt, or add a cup of *packed* brown sugar, or add some *confectioners* sugar, and so on.

Sure, these terms are cooking 101, but if you're 10-years-old and baking for the first time, this is a world of new terminology. Even measuring a cup of flour is difficult &mdash; does it have to be *exact*, and if so, how do you get it exact? You could use the flat edge of a knife to knock off the top peaks, but someone has to teach you how to do that. When my 10-year-old first started measuring flour, she went to great lengths to get it exactly 1 cup.

The world of software instruction is full of similarly confusing terminology. For the most part, you have to know your audience's general level so that you can assess whether something will be clear.

For example, does a user know how to *clear their cache*, or update *Flash*, or ensure the *JRE* is installed, or clone a git repository? Do the users know how to open a *terminal*, *deploy* a web app, import a *package*, *cd* on the command line, or *chmod* file permissions?

This is why checking over your own instructions by walking through the steps yourself becomes problematic. The first rule of usability is to know the user, and also to recognize that you aren't the user.

With developer documentation, usually the audience's skill level is far beyond my own, so adding little notes that clarify obvious instruction (such as saying that the `$` in code samples signals a command prompt and shouldn't be typed in the actual command, or that ellipses `...` in code blocks indicates truncated code and shouldn't be copied and pasted) isn't essential. But adding these notes can't hurt, especially when some users of the documentation are product marketers rather than developers.

The solution to addressing different audiences doesn't involve writing entirely different sets of documentation. You can link potentially unfamiliar terms to a glossary or reference section where beginners can ramp up on the basics. You can likewise provide links to separate, advanced topics for those scenarios when you want to give some power-level instruction but don't want to hold a user's hand through the whole process. You don't have to offer just one path through the doc set.

The problem, though, is learning to see the blind spots. If you're the only one testing your instructions, they might seem perfectly clear to you. Most developers also feel this way after they write something. They usually take the approach of rendering the instruction in the most concise way possible, assuming their audience knows exactly what they do.

But the audience *doesn't* know exactly what you know, and although you might feel like what you've written is crystal clear, because c'mon, everyone knows how to clear their cache, in reality you won't know until you *test your instructions against an audience*.

## Step 3: Test the instructions against an audience

Almost no developer can push out their code without running it through QA, but for some reason technical writers are usually exempt from QA processes. There are some cases where tech docs are "tested" by QA, but whenever this happens I usually get the strange feedback, as if a robot were testing my instructions.

QA people test to see whether the instructions are accurate. They don't test whether a user would understand the instructions or whether concepts are clear. And QA team members are poor testers because they already know the system too well in the first place.

Before publishing, every tech writer should submit his or her instructions through a testing process, a "quality assurance" process in the most literal sense of the word.

Strangely, few IT shops actually have a consistent structure for this doc-quality-assurance role. You wouldn't dream of setting up an IT shop without a quality assurance group for developers, but few technical writers have access to a dedicated editor or to a usability group to ensure quality.

When there are editors for a team, the editors usually play a style-only role, checking to make sure the content conforms to a consistent voice, grammar, and diction in line with the company's official style guide.

While conforming to the same style guide is important, it's not as important as having someone actually test the instructions. Users can overlook poor grammar &mdash; blogs and YouTube are proof of that. But users can't overlook instructions that don't work, that don't speak to the real steps and challenges they face.

I haven't had an editor for years. In fact, the only time I've ever had an editor was at my first tech writing job, where we had a dozen writers. But the editor there focused mostly on style.

I remember one time our editor was on vacation, and I got to play the editor role. I tried testing out the instructions and found that about a quarter of the time, I got lost. The instructions either missed a step, needed a screenshot, built on assumptions I didn't know, or had other problems.

The response, when you give instructions back to the writer, is usually the old "Oh, users will know that." The problem is that we're usually so disconnected with the actual user experience &mdash; we rarely see users trying out docs &mdash; we can't recognize the "users-will-know-how-to-do-that" statement for the fallacy that it is.

How do you test instructions without a dedicated editor, without a group of users, and without any formal structure in place? At the least, you can ask a colleague to try out the instructions.

### Ask a colleague to try out your instructions

Other technical writers are usually both curious and generous when you ask them to try out instructions. And when other technical writers start to walk through your steps, they recognize discrepancies in style that are worthy of discussion in themselves.

Although usually other technical writers don't have time to go through your instructions, and they usually share your same level of technical expertise, having *someone* test your instructions is better than no one.

Tech writers are good testing candidates precisely because they are writers instead of developers. As writers, they usually lack the technical assumptions that a lot of developers have (those assumptions that can cripple documentation).

Additionally, tech writers who test your instructions know exactly the kind of feedback you're looking for. They won't feel ashamed and dumb if they get stuck and can't follow your instructions. They'll usually let you know where your instructions are lacking. *I got confused right here because I couldn't find the X button, and I didn't know what Y meant,* they'll say. They know what you need to hear.

In general, it's always good to have a non-expert test something rather than an expert, because experts can often compensate for shortcomings in documentation with their own expertise. Novices can't compensate.

Another reason tech writers make good testers is because this kind of activity fosters good team building and knowledge sharing. At a previous job, I worked in a large department that had, at one time, about 30 UX engineers. The UX team held periodic meetings during which they submitted a design for general feedback and discussion.

By giving other technical writers the opportunity to test your documentation, you create the same kind of sharing and review of content. You build a community rather than having each technical writer always work on independent projects.

What might come out of a user test is more than highlighting shortcomings about poor instruction. You may bring up matters of style, or you might foster great team discussions through innovative approaches to your help. Maybe you've integrated a glossary tooltip that is simply cool, or an embedded series button. When other writers test your instructions, they not only see your demo, they understand how helpful that feature is in a real context.

### Should you watch when users test?

One question in testing users is whether you should watch them in test mode. Undeniably, when you watch users, you put some pressure on them. Users don't want to look stupid when they're following what should be relatively simple instructions.

But if you don't watch users, the whole testing process is much more nebulous. Exactly *when* is a user trying out the instructions? How much time are they spending on the tasks? Are they asking others for help, googling terms, and going through a process of trial and error to arrive at the right answer?

If you watch a user, you can see exactly where they're getting stuck. Usability experts prefer it when users actually share their thoughts in a running monologue. They'll tell users to let them know what's running through their head every now and then.

In other usability setups, you can turn on a web cam to capture the user's expression while you view the screen in a gotomeeting screenshare. This can allow you to give the user some privacy while also watching them directly.

In my documentation projects, I'm sorry to admit that I've veered far away from usability testing. It's been years since I've actually tested my documentation this way, despite the eye-opening benefits I get when I do it. (Writing about it now, I'm making serious plans to mend my ways.)

At some point in my career, someone talked me into the idea of "agile testing." When you release your documentation, you're basically submitting it for testing. Each time you get a question from users, or a support incident gets logged, or someone sends an email about the doc, you consider that feedback and potential bugs to log against the documentation. (<i>And if you don't hear anything, then the doc must be great, right?</i>)

Agile testing methods are okay. You should definitely act on this feedback. But hopefully you can catch errors *before* they get to users. The whole point of any kind of quality assurance process is to ensure users get a quality product.

Additionally, the later in the software cycle you catch an error, the more costly it is. For example, suppose you discover that a button or label or error message is really confusing. It's much harder to change it post-release than pre-release. I particularly hate it when the interface has typos or misspellings that I have to follow in documentation commands just to keep the two in sync. (For example, "Click the **Multi tenancy** button.")

## Enjoyment benefits from testing

One of the main benefits to testing is that it makes writing documentation much more enjoyable. There's nothing worse than ending up as a secretary for engineers, where your main task is to listen to what engineers say, write up notes, send it to them for review, and listen to their every word as if they're emperors who give you a thumbs up or thumbs down. That's not the kind of technical writing work that inspires or motivates me.

Instead, when I can walk through the instructions myself, and confirm whether they work or not, that's when things become interesting. Actually, the more you learn about the knowledge domain itself, the work of technical writing increases dramatically.

In contrast, if you just stick to technical editing, formatting, publishing, and curating &mdash; these activities are all worthwhile, but they are not fulfilling as a career. Only when you get your synapses firing in the knowledge domain you're writing in, as well as your hands dirty testing and trying out all the steps and processes, does the work of technical writing start to become engaging.

## Accounting for the necessary time

Note well that it takes time to try out the instructions yourself and with users. It probably doubles or triples the documentation time. You don't always have this time before release. I can't say that I've tested out all the different parts of my documentation, because I have four different programming languages across various platforms, but for the doc that I do test, it makes a world of difference.

One way to shorten the testing period is by leveraging the test scripts used by your QA team. These test cases often give you a clear picture about the functionality provided by the system, along with sample calls to see if each piece works. QA scripts are usually much more thorough than you need, but they're helpful in pointing you in the right direction.