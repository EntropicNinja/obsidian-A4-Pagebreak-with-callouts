
- Natural page breaks at A4 boundaries (no forced breaks at headings)
- Manual page break: type > [!pagebreak] anywhere in your note
  - Invisible in reading view, forces a page break in PDF export
  - Can be used as many times as needed
  - All clean-break rules apply from that point forward
- Headings never stranded at bottom of page (widow protection)
- Paragraphs that would end near the bottom move to the next page instead
- Code blocks, tables, images, and callouts never split across pages
- hr elements converted to explicit page breaks

> [!Note]
> Originally found [obsidian-pagebreak](https://gist.github.com/liamcain/81679412643690a7cdd13dff4dc909ce) but then noted that it was updated by [robotii](https://gist.github.com/robotii/aa580b1c00937d37c44f1033034b0e1a) to:
> > [!Quote] Properly select the first h1 and remove page break before it.
> > [!Quote] Added support to not split adjacent headings.
> > [!Quote] Change background colour to white for better PDF generation.
>

I wanted the snippet to respect A4 boundries and to not cut things like codeblocks or callouts in half, or have a Heading at the bottom of a page with only 2-4 lines of text.
I also wanted to have a way for the user to manually add a page break but that it still respect the above stipulations.

> [!Caution]
> One caveat: `orphans` and `widows` are well-supported in Chromium/Electron, but the exact behaviour depends on line height and font size. 
> If you find a particular paragraph still splits awkwardly, bumping the value to 5 or 6 usually sorts it.

> [!TIP]
> If you want to tweak things, `orphans`/`widows` number on **paragraphs** (higher = more aggressive forward-pushing) and `margin` in **@page** (20mm is fairly standard but you may prefer a bit more breathing room).

