### The Thinking & The Engineering

This project didn’t start with a model. It started with an 800-page psychology textbook and one slightly dangerous thought: “How hard can this be?”

I wasn’t trying to learn psychology. I was trying to reverse-engineer it.

When you build a RAG system, the real work isn’t just embeddings and vector stores. It’s structure. Retrieval quality lives and dies by structure. So I opened the PDF not as a reader, but as an engineer looking for patterns.

The first good sign? A table of contents.

For a reader, that’s navigation.
For me, that’s metadata gold.

Chapters. Sections. Subsections. Hierarchy. Signals.

That table of contents told me the book was already logically organized. Which meant if I could align raw PDF text with that structure, I wouldn’t just have chunks — I’d have semantically grounded chunks.

So I pulled the PDF into PyPDF and started extracting text. That’s when the fun began.

PDFs don’t care about your feelings.
They care about layout.

There were no clean delimiters. No reliable heading markers. No structural tags. No consistent formatting. Just text and newline characters doing their best impression of organization.

Newline.
Newline.
Newline.

That was basically my only delimiter.

And if you’ve worked with PDFs, you know: newline is not structure. It’s chaos in disguise.

Paragraphs break randomly.
Headings sometimes look like body text.
Line wraps pretend to be sentence breaks.

At that moment I had two options:

1. Pretend newline equals structure and pray retrieval works.
2. Or actually engineer the structure.

So I chose engineering.

Instead of chunking blindly, I started aligning text with the table of contents. I mapped chapters. Then sections. Then section headings. I treated the book like a hierarchical dataset instead of a blob of text.

Because in RAG, chunking isn’t about splitting text.

It’s about preserving meaning boundaries.

That shift — from “split by newline” to “respect semantic hierarchy” — is what turned this from a PDF experiment into an actual retrieval system.

And that’s when the project stopped being “let’s try RAG” and became:

Let’s make this thing actually retrieve like it understands the book.

That’s where the engineering really began.
