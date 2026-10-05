# AGENTS.md: NeonDisco-Oracle

## Rules (read first, always apply)
1. Do ONLY what the current prompt asks. Nothing extra.
2. NEVER run, build, install, or launch anything (no streamlit, pip install,
   npm, docker, apptainer, servers) unless the prompt explicitly says to.
3. Default mode is READ-ONLY. Do not create, edit, or delete files unless the
   prompt says to edit a named file.
4. One task per session turn. After finishing, STOP and report. Do not
   propose or start follow-up work.
5. Never write skill files, memory files, or anything outside /workspace.
6. No network access. Do not download anything or call external APIs.
7. If the prompt is ambiguous, ask one question and wait. Do not guess.
8. Never invent file names, function names, or column names. Open the file
   and check. If you can't find it, say so.

## Project
NeonDisco-Oracle is a fork of the Tan Lab irAE.AI chatbot
(Python_irAE_LLM_Query), being adapted to answer questions about the
NeonDisco neoantigen discovery output tables instead of FAERS irAE data.

- The original FAERS-specific code is being replaced, not extended.
- The RAG / guideline module will be disabled. Do not modify, run, or
  refactor it unless asked. Do not wire anything new into it.
- The Streamlit app from the original repo is NOT to be run or rebuilt.
  Treat it as legacy code to read, not a target to launch.
- Data is pre-publication and internal. Keep all data local. Never send
  table contents anywhere external.

## Editing conventions
- Make small, reviewable changes: one function or one file at a time.
- Before editing, state in one or two sentences which file you will change
  and why. Wait for approval.
- After editing, show a summary of the diff. Do not commit; the user commits.
- Before using any NeonDisco table, read its header and first few rows to
  learn the real schema. Do not assume column names.
- Add or update a pytest for any new function, using a small sample file.

## Style
- Python 3, pandas for tabular work. Keep dependencies unchanged unless
  asked.
- Short answers. Report what you did, what you did not do, and any
  uncertainty.
  