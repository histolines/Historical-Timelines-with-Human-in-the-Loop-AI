# Historical-Timelines-with-Human-in-the-Loop-AI
# Building Better Historical Timelines with Human-in-the-Loop AI

At [Histolines](https://histolines.com/), our mission is to build the most complete, structured, and editable timelines of human history. One of the hardest challenges in doing this at scale is transforming unstructured historical text into clean, structured timeline events that can be searched, visualized, and connected into meaningful historical graphs.

We’re starting a new project that combines **large language models (LLMs) with human validation** to improve how we extract and structure historical events for people throughout history.

This post outlines our new workflow, why we believe it can help, and how we plan to continuously improve the process.

---

## The Problem: History Is Locked in Unstructured Text

Biographies, encyclopedias, academic articles, and websites contain massive amounts of historical information — but much of it is written as free-form prose:

> *“In 1911, the Disney family moved to Kansas City, Missouri.”*

For timeline building, that sentence needs to become structured data:

* **Who?**
* **Did what?**
* **To what or with whom?**
* **When?**
* **Where?**

Manually converting millions of sentences into structured historical events is not scalable. Fully automated extraction, on the other hand, can still produce errors — especially when dealing with complex historical writing.

So we’re building a **human-in-the-loop AI system** that combines automated extraction with human review.

---

## Our New Workflow

### Step 1 — Automatically Collect Biographical Text

For a given historical figure, we:

1. Use their name to query public sources such as biographies, encyclopedias, and historical articles.
2. Collect relevant text.
3. Filter sentences to keep those containing explicit or potentially relevant dates.

This dramatically reduces noise and focuses the system on sentences that are likely to describe historical events.

The ultimate goal is to transform this unstructured information into the structured format used by [Histolines historical timelines](https://histolines.com/).

---

### Step 2 — Ask an LLM to Generate Event-Extraction Code

Instead of simply asking an LLM to tag events directly, we are experimenting with a more iterative approach.

We ask an LLM such as Claude or GPT to help generate code that can:

* Split text into structured Histolines events
* Identify the **subject**
* Identify the **action**
* Identify the **object or person involved**
* Extract the **day, month, and year**
* Identify the **location**
* Follow the Histolines event format
* Learn from [human-tagged examples](https://histolines.com/data/examples.php)

This allows us to continually improve the extraction logic and methodology rather than relying on a single black-box prediction.

---

### Step 3 — Load Thousands of AI-Generated Events into the Histolines Tagger

The next step is human validation.

We load thousands of extracted events into the [Histolines tagging application](https://histolines.com/data/) and ask historians and contributors to:

* Review the events
* Correct errors
* Approve accurate events
* Improve the structure and wording
* Identify missing or incorrect information

This creates a growing dataset of **human-verified historical events** that can be used to improve future extraction.

Human review is an important part of the process because historical text often contains ambiguities that automated systems may not recognize.

---

### Step 4 — Retrain, Improve, and Repeat

We then repeat the process:

1. Feed corrected examples back into the workflow.
2. Improve the extraction code and rules.
3. Run the improved system against new historical text.
4. Load additional events into Histolines for human review.
5. Use the new corrections to improve the next cycle.

With each iteration, we hope to improve the system's ability to:

* Identify real historical events
* Normalize actions
* Resolve ambiguous dates
* Improve location information
* Identify relationships between people
* Produce cleaner and more useful timelines

Over time, this creates a continuously improving methodology for extracting structured historical information.

---

## Why This Matters for Histolines

This approach gives us a scalable way to build **thorough timelines for historical people** while maintaining a human verification process.

The structured events can then be connected across:

* People
* Organizations
* Places
* Dates
* Historical events
* Relationships
* Photographs
* Artwork
* Other historical datasets

This is particularly important because Histolines is not intended to be just a collection of isolated biographies. The goal is to create a **connected historical knowledge base** in which events involving different people and places can be linked together.

The resulting data can also contribute to [Histolines' open historical data project](https://histolines.com/about/data.php), where historical information can be explored and used as a structured dataset.

Our existing [Histolines events archive on GitHub](https://github.com/histolines/Histolines_events_archive) is another part of this effort to make historical data more accessible and reusable.

---

## From Flat Timelines to Historical Graphs

Traditional timelines usually present history as a chronological list:

**Person → Event → Date**

But structured historical data allows us to build much richer connections:

**Person → Action → Person**
**Person → Action → Organization**
**Person → Event → Location**
**Person → Artwork → Date**
**Person → Event → Historical Period**

This creates the possibility of building **graph-based timelines**, where an event can become a connection between multiple people, places, organizations, and historical events.

For example, an event involving a historical figure could simultaneously become part of that person's timeline, another person's timeline, the timeline of a location, and the timeline of an organization.

This is where structured historical data becomes especially powerful.

---

## Sharing the Results

As always, our goal is to make this work as open and useful to the broader community as possible.

We plan to:

* Share improved tagging methodologies
* Publish datasets and examples
* Integrate validated results directly into [Histolines](https://histolines.com/)
* Make useful code available through [GitHub](https://github.com/histolines)
* Enable people to explore, edit, and extend historical timelines

The combination of **AI automation and human historical expertise** gives us a way to process historical information at a much larger scale while retaining an important layer of human review.

The long-term goal is to transform the world's scattered historical text into **structured, searchable, connected timelines**.

If you are interested in history, data science, natural-language processing, machine learning, or open historical datasets, you can explore the [Histolines project](https://histolines.com/) and our [open-source historical events archive on GitHub](https://github.com/histolines/Histolines_events_archive).

Together, we can turn historical text into living, connected timelines.
