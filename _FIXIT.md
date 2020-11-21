> Jim Carroll |
> 10/13/2020 |
> [GitHub Profile](https://github.com/pulamusic)

---

# Fixing Liquid syntax errors that keep popping up after running `jekyll serve`

Open **`index.html`** and fix the following syntax errors

```zsh
  n "{{#foreach tags}}" in index.html
      Liquid Warning: Liquid syntax error (line 44): Unexpected character # i
  n "{{#if @first}}" in index.html
      Liquid Warning: Liquid syntax error (line 44): Unexpected character / i
  n "{{/if}}" in index.html
  n "{{/foreach}}" in index.html
      Liquid Warning: Liquid syntax error (line 66): Unexpected character # i
  n "{{#foreach tags}}" in index.html
      Liquid Warning: Liquid syntax error (line 66): Unexpected character # i
  n "{{#if @first}}" in index.html
      Liquid Warning: Liquid syntax error (line 66): Unexpected character / i
  n "{{/if}}" in index.html
      Liquid Warning: Liquid syntax error (line 66): Unexpected character / i
  n "{{/foreach}}" in index.html
      Liquid Warning: Liquid syntax error (line 88): Unexpected character ! i
  n "{{!! After all the posts, we have the previous/next pagination links }}"
   in index.html
```

removed from line 25
<!-- , tagged on {{foreach tags}}<span class="post-tag-{{slug}}">{{if first}}{{else}}, {{if}}<a href="/tag/{{slug}}">{{name}}</a></span>{{foreach}} -->

removed from line 41
<!-- , tagged on {{foreach tags}}<span class="post-tag-{{slug}}">{{if first}}{{else}}, {{if}}<a href="/tag/{{slug}}">{{name}}</a></span>{{foreach}} -->

removed from line 92
<!-- {{!! After all the posts, we have the previous/next pagination links }}
{{pagination}} -->
