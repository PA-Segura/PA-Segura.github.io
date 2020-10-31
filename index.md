#+TITLE: Jekyll and Org together
#+LAYOUT: post
#+TAGS: jekyll org-mode "tag with spaces"

This is a blog post about Jekyll and Org mode.

** org-table demo 

   | a | b | c | d | e |
   |---+---+---+---+---|
   | 1 | 2 | 3 | 4 | 5 |

** Liquid demo 
   #+liquid: enabled
   #+foo: hello world
   {{ page.foo }}

   or

   {{ site.time | date_to_xmlschema }}
   
** Code highlighting
   Jekyll-org also offers powerful support for code snippets:
   ##+begin_src  ruby 
     def print_hi(name)
       puts "Hi, #{name}"
     end
     print_hi('Tom')

     #=> prints 'Hi, Tom' to STDOUT.
   ##+end_src

# Easy Markdown to Github Pages
* Hello world

lets see how it goes

** this is a subtitle

## Is this markdown or org..