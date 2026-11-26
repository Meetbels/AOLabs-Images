# PROMPTS.md

Verbose, append-only archive of prompts. The author's messages are copied verbatim, with a
one-line outcome. This is a record for repeating the process in another AI tool, not
instructions. AI assistants should not read it unless asked.

---

## 2026-11-26: project brief (from Chatai)

> It will have a frontend and a backend component.
> Build a web app that uploads and displays files on an AWS S3 bucket.
> Image files are more than ok.
> When a file is selected, have a preview and display metadata information about it.
> Have some analytics graphs/charts about the files like their type and size distributions
> Vega-Lite is a good option for the graphs/charts
> You can use the backend to generate the data for the Vega-lite, and use pandas library to do that.
>
> Deliverables:
> 1. Build a frontend with Typescipt and React. Also use Tailwind for the CSS styling.
> 2. Build a backend with Python FastAPI that also uses AWS SDKs.
> 3. Signup for a free AWS account.
> 4. Deploy the frontend and the backend using a Cloud Formation Template.
>    - Frontend can be a SPA (Single Page Application)
>    - Backend can be a Fargate task
> 5. While doing these, setup your development environment using VSCode.
>    - Make sure that you have your debuggers running locally
>    - Have some unit tests running.
>
> Also, for your specific project,
> 1. Try to do more detailed analysis in the backend side using pandas.
> 2. You can extend the frontend side a bit by adding custom metadata files in JSON format and using these metadata to do more analysis.
>    - Feel free to make up anything like adding some random data to the images like location, resolution, etc.
>    - The focus on more about processing/generation a lot of JSON data and summarising them.
>    - Have a look at ball and player tracking data in tennis and maybe associate them to the images; i.e. an image of a forehand shot and metadata includes the tracking data samples.

Outcome: the brief. Not yet built.

---

## 2026-11-26: initialise docs

> for process, are we having that there just to document what has been done? so AI can pickup where we left off?
> I feel like we could go for something even simpler just to minimize ai bloat (becuase you will be writing all of it probably), whats the reasonable minimal
> I'd also like to keep a much more verbose and unfiltered PROMPTS.md, how would this change things for u
> the empty md fil;es exist, just initialise them please
> yes please

Outcome: CLAUDE.md, PROCESS.md and PROMPTS.md initialised. CLAUDE.md moved to the repo root; committed on branch `chore/init-docs`. Earlier conceptual Q&A (CloudFormation, Fargate, FastAPI, Vega-Lite, S3 vs MongoDB, Docker) not logged.
