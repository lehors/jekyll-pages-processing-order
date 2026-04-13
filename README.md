# Jekyll's pages processing order test

The files `c.md` and `e.md` are the same. The only difference is their name. They loop through `site.pages`
and using a simple test (looking for markdown `#`) determines whether `page.content` is rendered or not rendered
and display the finding.

Based on this test it appears that pages are processed in alphabetical order. All pages before the page doing the
test are rendered and not the ones after. So, the same page content gives a different result depending on the filename
and where it stands in alphabetical order.

## c.md
```
a.md rendered

b.md rendered

c.md unrendered

d.md unrendered

e.md unrendered

main.scss rendered

/feed.xml rendered
```

## e.md
```
a.md rendered

b.md rendered

c.md rendered

d.md rendered

e.md unrendered

main.scss rendered

/feed.xml rendered 
```
