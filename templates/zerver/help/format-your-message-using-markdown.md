# Format your messages

[//]: # (All screenshots here require line-height: 22px and font-size: 16px in .message-content.)
[//]: # (Requires some additional fiddling for the LaTeX picture, inline code block, and maybe a few others.)

Zulip uses a variant of
[GitHub Flavored Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
to allow you to easily format your messages.

* [Emphasis](#emphasis)
* [Lists](#lists)
* [Links and images](#links)
* [Code blocks](#code)
* [LaTeX](#latex)
* [Quotes](#quotes)
* [Spoilers](#spoilers)
* [Emoji and emoticons](#emoji-and-emoticons)
* [Mentions](#mentions)
* [Status messages](#status-messages)
* [Mention a time](#mention-a-time)
* [Tables](#tables)
* [Paragraphs and lines](#paragraphs-and-lines)

## Emphasis

```
**bold**, *italic*, and ~~strikethrough~~ text
***~~All three at once~~***
```

![](/static/images/help/markdown-emphasis.png)


## Lists

Bulleted lists
```
* bulleted lists
  * with sub-bullets too
  * sub-bullets start with 2 spaces
    * start sub-sub-bullets with 4 spaces
* multi
line
bullet
- dashes and
+ pluses are ok too
```

![](/static/images/help/markdown-bullets.png)

Numbered lists

```
1. numbered lists
1. increment automatically
1. one more
```

![](/static/images/help/markdown-numbered-lists.png)


## Links

Zulip auto-linkifies URLs and valid stream names. You can also add a
[custom linkifier](/help/add-a-custom-linkification-filter) to link
patterns like `#1234` to your ticketing system.

```
Auto-detected URL: zulip.com
Named link: [Zulip homepage](zulip.com)
Stream: #**stream name**
Topic: #**stream name>topic name**
Custom linkifier: #1234 (links to ticket 1234 in your ticketing system)
```

![](/static/images/help/markdown-links.png)

## Images

See [Share and upload files](/help/share-and-upload-files) to learn more
about dropping, pasting, and attaching images.

```
[A whale of a good time](https://your.zulip.domain/user_uploads/1/46/IPvysqXEtiTG1ZdNBrwAZODi/whale-time.png)
```

![](/static/images/help/markdown-image.png)

## Code

~~~
Inline: `let x = 5`

Code block:
```
def f(x):
   return x+1
```

Syntax highlighting:
```python
def fib(n):
    # TODO: base case
    return fib(n-1) + fib(n-2)
```
~~~

![](/static/images/help/markdown-code.png)

You can also use `~~~` to start codeblocks, or just indent the code 4 or more spaces.

Zulip supports syntax highlighting for hundreds of languages, and a
typeahead will pop up when you start typing after the ` ``` `. If you can't
find your language, search for it [here](https://pygments.org/docs/lexers/)
and try the **short names** listed for the lexers for your language.

Organization administrators can also configure a default syntax
highlighting language.  In this configuration, one can use ````text`
to display content without any syntax highlighting.

## Latex
~~~
Inline: $$O(n^2)$$

Displayed:
``` math
\int_a^b f(t)\, dt = F(b) - F(a)
```
~~~

![](/static/images/help/markdown-latex.png)

Zulip's LaTeX rendering is powered by [KaTeX](https://katex.org).
Their [support table](https://katex.org/docs/support_table.html) is a
helpful resource for checking what's supported or how to express
something.

## Quotes

~~~
> a multi-line
quote on two lines

normal text

```quote
A multi-paragraph

quote in two paragraphs
```
~~~

![](/static/images/help/markdown-quotes.png)

## Spoilers

You can use spoilers to hide content that you do not want to be visible until
the user interacts with it.


~~~
Normal content in message

```spoiler Spoiler Header
Spoiler content. These lines won't be visible until the user expands the spoiler.
```
~~~

The spoiler will initially display in a collapsed form:

![](/static/images/help/spoiler-collapsed.png)

Clicking the arrow will expand the spoiler content:

![](/static/images/help/spoiler-expanded.png)

## Emoji and emoticons

To translate emoticons into emoji, you'll need to
[enable emoticon translations](/help/enable-emoticon-translations).
You can also [add custom emoji](/help/add-custom-emoji).

```
:octopus: :heart: :zulip: :)
```

![](/static/images/help/markdown-emoji.png)

## Mentions

Learn more about mentions [here](/help/mention-a-user-or-group).
The numbers will be added automatically by the typeahead if needed for disambiguation.

```
Users: @**Polonius** or @**Zoe|2132** (two asterisks)
User group: @*support team* (one asterisk)
Silent mention: @_**Polonius** (@_ instead of @)
```

![](/static/images/help/markdown-mentions.png)

## Status Messages

```
/me is away
```

![](/static/images/help/markdown-status.png)

## Mention a time

When collaborating with people in another timezone, you often need to
express a specific time clearly. Rather than typing out your timezone
and having everyone translate the time in their heads, in Zulip, you
can mention a time, and it'll be displayed to each user in their own
timezone (just like the timestamps on Zulip messages).

A date picker will appear once you type `!time`.

```
Our next meeting is scheduled for !time(2020-05-28T13:30:00+05:30)
```

A person in San Francisco will see:

> Our next meeting is scheduled for *Thu, May 28 2020, 1:00 AM*.

While someone in India will see:

> Our next meeting is scheduled for *Thu, May 28 2020, 1:30 PM*.

## Tables

The initial pipes (`|`) are optional if every entry in the first column is non-empty.
The header separators (`---`) must be at least three dashes long.

```
|| yes | no | maybe
|---|---|:---:|------:
| A | left-aligned | centered | right-aligned
| B |     extra      spaces      |  are |  ok
| C | **bold** *italic* ~~strikethrough~~  :smile:  ||
```

![](/static/images/help/markdown-table.png)

## Paragraphs and lines

```
One blank space for a new paragraph
New line, same paragraph

New paragraph

---, ***, or ___ for a horizontal line
Over the line

---

Under the line
```

![](/static/images/help/markdown-paragraph.png)

## In-app help

A summary of the formatting syntax is available in-app.

{start_tabs}

{!start-composing.md!}

1. Click the A (<i class="fa fa-font"></i>) icon at the bottom of the compose box.

{end_tabs}

## Related articles

* [Create a poll](/help/create-a-poll)
