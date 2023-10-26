# Anki deck for A Course in Contemporary Chinese (當代中文課程)

Ankiweb: https://ankiweb.net/shared/info/1466478713

Anki deck with vocabulary terms from a taiwanese Mandarin textbook series [A Course in Contemporary Chinese](http://www.mtc.ntnu.edu.tw/eng/book/A_Course_in_Contemporary_Chinese.html) (當代中文課程) *"dangdai zhongwen"* by NTNU, book 1 to book 6 complete, including recorded audio from book's website.

This is a compilation from several online sources: vocabulary slides and quizlet decks from book's [website](http://mtc.ntnu.edu.tw/chinese-resource.htm), as well various community decks floating around. Differences between the sources were checked against the books (1st edition, 2015-2018), even official decks have some couple hundred diffs against them, so hopefully this is the most complete and true to the book vocabulary deck for this book series that you could find online to date.

Part of speech (POS), names and phrase terms are annotated according to the book. There's a unique sort ID key to identify book, lesson, dialogue/text and term index, that you can use to filter for specific books/lessons e.g.:
  - `B1L15-II-10`: book 1, lesson 15, dialogue II, term 10;
  - `B5L05-I-0-01`: book 5, lesson 5, text I, foreword terms (found in B5-B6), term 1;
  - `B6L01-III-T-06`: book 6, lesson 1, text III, technical terms (found in B6, mostly names), term 6.

Simplified variants of terms are also provided, mostly from vocabulary slides. But note that this is primarily a traditional Chinese textbook series and for taiwanese Mandarin variety.

A few deliberate differences from book content:
  - phrase terms for B1-B4 are annotated with `POS:Ph` for consistency with B5-B6 (the first four books themselves otherwise don't list any POS for them);
  - terms with multiple POS use "/" separator for consistency (books sometimes use comma);
  - a few minor obvious typos in book corrected, some simplified chars in slides and apostrophe usages in pinyin fixed.

Tags:
  - `Name`: terms from "Names" / "People in the dialogue" sections (B1-B4) + manually tagged named entities (B5-B6);
  - `Character`: subset of names - book character names only ("People in the dialogue"). Don't need to care about these if you're not going to read dialogues in the book.

Audio comes from book's website - recorded sounds by book's authors. Slicing into individual terms done thanks to "[all vocabs](https://ankiweb.net/shared/info/2118503187)" ([github](https://github.com/jiru/ccc/tree/main)). Card template also comes from the same deck, slightly revised, just hanzi->pinyin/meaning template so you don't have to do much cleanups after importing if you only want to use this deck for reference data. Taiwan Ministry of Education's standard Kaiti font is included with proper Taiwan standard variants of characters - the same main learning font you'd see in most taiwanese textbooks.

`Variants`: for terms with multiple writing/pinyin variants and a few other oddities, a more machine-friendly list of expanded variants as a JSON list `[["term", "pinyin"], ...]`, as the book is inconsistent in formatting those. If using this deck for an automatic analysis (such as merging with other sources or your anki decks), you might find this field useful.

## Files

- `dangdai.csv`: deck in .csv format. Can be loaded to Anki or used in scripts.
- `dangdai-pleco.txt`: version for importing to Pleco as flashcards or a user dictionary:
  - Settings > Manage Dictionaries > Add User > New (Existing won't work with .txt)
  - Settings > Manage Dictionaries > Import Entries > select .txt
- `data`: inputs and intermediate files
  - `book.tsv`: entries with diffs reviewed against the book. The correct entry matching the book is in the file.
  - `errata.tsv`: indentional corrections for some typos.
  - `variants.tsv`: manually expanded entries with multiple spellings/pinyin to a more uniform machine-parseble format.
- `slides.ipynb`, (`extdecks.ipynb`), `audio.ipynb`, `merge.ipynb`: pipeline, run in this order.
