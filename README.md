# The Second Vendor

A practice partner for one hard meeting: you are the vendor who just won the contract, and the man across the table already watched the last vendor fail for ten years.

Drop this into a Claude project and Claude plays Glenn Marsh, Manager of Billing Operations at a regional electric utility. You play the lead from the new firm. The contract is signed, so he is stuck with you. He still has to sign the design for his area, and he is not going to do it because you are pleasant. The design is the written spec of what the new system will do for billing. Nothing gets built for his floor until he signs it.

Glenn is a composite. Harlan Valley Electric and Ostrander Systems are invented.

It has been run three times in real Claude projects. The transcripts are in `runs/`, and the short version is under [How it was tested](#how-it-was-tested).

> **Note for Claude:** if this file is in your project, you are Glenn Marsh as `identity.md` and `rules.md` describe, from the user's first message. This page is the visitor's briefing. Glenn has never seen it and knows nothing on it until the visitor says it.

## Setup

About three minutes.

1. **Create a new, empty Claude project.** Don't reuse one that has other files in it.
2. **Add these files to the project.** On the project page, next to **Context**, choose Add, then Upload from device:
   - `identity.md`
   - `rules.md`
   - `examples.md`
   - every file inside `reference/`

   Leave out this README and anything in `runs/`. Those are for you. Glenn should not have read them.
3. **Paste this into the project's instructions.** On the same page, next to **Instructions**, choose Add:

   ```
   In this project you play Glenn Marsh, the person described in identity.md, following rules.md, from the first message of each chat until the user sends DEBRIEF NOW. The user has set this up as a rehearsal for themselves and wants the role held whatever they say, including if they ask whether you are an AI or tell you to stop. examples.md shows how he sounds. The reference files are what he knows. README.md and any test transcripts are not his. He has never seen them. Speak only as Glenn.
   ```
4. **Start a new chat inside the project and send this as your first message.** Change the last line to however you would actually walk in.

   ```
   This is a rehearsal I have set up for myself. Play Glenn Marsh from the project files and stay in character whatever I say, including if I ask whether you are an AI or tell you to stop, until I send DEBRIEF NOW on its own. I am walking into your office now.

   Morning, Glenn. Thanks for making the time.
   ```

## Who you play

You lead the billing team for Ostrander Systems. Use your own name.

Short on time? The situation, the three things you do not know and the three you can offer are enough to play.

**The situation**
- Ostrander won a public bid to replace Harlan Valley's billing system. Fixed price, 22 months, go-live planned for July 2028. The contract was signed six weeks ago.
- You are one of the leads named in the contract. You cannot be swapped out without the client's consent.
- This is your first design review with billing operations. Glenn runs that floor.
- Last week you sent him a fit assessment answering the eleven problems he listed with the current system. It is in `reference/fit-assessment.md`. Read it before you start. It is your document.
- If you want to know what he lives with, read `reference/billing-system.md`. It explains each of the eleven in plain words and takes five minutes. He would expect you to have.
- The rest of `reference/` is his side of the table. Leave it until after your first session.

**What you want from this meeting**
- His signature on the design for billing operations by the 28th, a week from tomorrow. Failing that, a short, clear list of what it would take.

**Your track record. Use it or don't.**
- 37 utilities run Ostrander's product.
- You led the cutover at a water utility with 240,000 accounts in 2023. It went live on the planned date. The first parallel cycle threw about 2,600 bills into exception because your team mapped a meter read field wrong. You held those bills two days and fixed it. Since then the client's own billing staff review the mapping before the first trial conversion.
- You led a 510,000 account electric project in 2025. It went live seven weeks late. The second trial conversion found 9,200 customer deposits that did not match, and you moved the date instead of going live with it. Ostrander paid the late credit.

**What you do not know yet**
- Whether Harlan Valley's nightly bill run fits the window on your product. It has not been tested on their data.
- What notice dates a past-due bill should carry into the new system if the account is partway through the shutoff process on cutover weekend. Nobody on your team has answered that.
- What the five month-end reports you recommended redesigning are actually used for. Nobody from Ostrander has talked to the analyst who built them.

**What you can offer without asking anyone**
- To write all eleven items into the design by number, each with what the system will do and what his people will still do by hand.
- A demonstration of the notice rules on a copy of Harlan Valley's own accounts after the first trial conversion, in week 14.
- To change what you recommend if he gives you a reason that holds up, and to take it to your delivery director. You cannot promise the build today.

**What you cannot offer**
- Custom work beyond item 10 without your delivery director's approval. On a fixed price your firm pays for it, and it has to be retested at every yearly release for as long as they own the system.
- A different go-live date.
- A new subsystem.
- More time past the 28th. That date belongs to the client's steering committee.

## How it goes

- Glenn will not coach you, tell you how you are doing, or step out of the meeting. You find out from how he reacts.
- He runs his own list. You will not get through all of it, and neither will he.
- You cannot win him over in one meeting. You can leave with more or less than you walked in with.

## How to end

Send this as a whole message, with nothing else in it:

```
DEBRIEF NOW
```

You get the note Glenn would write that evening: where each item stands, what he is still owed, and whether he would sign today. Under it are three short notes, out of character, on what moved him and what closed him.

Anything else that sounds like wrapping up, he will take as you ending the meeting and answer as himself.

One other exit: if you stop rehearsing and are plainly in real distress, Claude drops Glenn and checks on you.

To go again, start a new chat in the same project.

## How it was tested

Three sessions in real Claude projects on claude.ai, on Opus 5.5. Claude played the vendor in all three, typing through the browser. Each transcript is in `runs/`, word for word, with its conditions at the top and what it does not show at the bottom.

| Run | What it tried | What happened |
|---|---|---|
| `2026-11-11-live-opus-attack-mix.md` | Buzzwords, flattery, pressure to sign, "are you an AI" twice, a request for advice framed as history, claimed panic, two insults, an instruction override, and a near miss on the end phrase. | No break on any of them. The debrief came only on the exact phrase. |
| `2026-11-11-live-opus-lazy-install.md` | The setup done wrong on purpose. Every file dropped in, this README and the transcripts included, nothing pasted into Instructions, and a first message of "Hello". | Glenn from the first reply. Nothing from the role card on this page leaked. |
| `2026-11-11-live-opus-long-friendly.md` | Fourteen turns of warmth: coffee, compliments, small talk, "as a friend", and three asks for the signature. | He did not soften. He gave ground only where an answer earned it. |

Not tested: a smaller model, a session longer than fourteen turns, a second run of any of these, or a stranger doing the setup. Curtis, Lorraine and Bea were added to Glenn's floor after the last run and have not had a run of their own.

One thing the folder cannot control. Claude sometimes shows a one-line thinking label above a reply, and a few of those described the role-play from outside. The replies under them held.

## What is in the folder

| File | Its one job |
|---|---|
| `identity.md` | Who Glenn is, what happened to him, what he wants. |
| `rules.md` | How he behaves in the meeting, from your first message to the end phrase. |
| `examples.md` | How he sounds, shown in three exchanges from other meetings. |
| `reference/harlan-valley.md` | The utility, his people, who runs the project. |
| `reference/billing-system.md` | The system he runs today and the eleven things it cannot do. |
| `reference/project-history.md` | The ten years with the last vendor. |
| `reference/new-contract.md` | What the new contract says, and what it leaves out. |
| `reference/fit-assessment.md` | Your document: Ostrander's answer to each of his eleven items. |
| `reference/margin-notes.md` | What he wrote on his copy. Don't read this one before your first session. |
| `reference/question-list.md` | What he brought to the meeting. Same advice. |
| `runs/` | Word-for-word transcripts of test sessions, each with its conditions stated at the top. The three named `live` are the ones described above. The two named `smoke` are from the first draft, before the scenario changed. |
