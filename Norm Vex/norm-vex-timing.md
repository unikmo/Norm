# Stand-up timing for Norm Vex

Timing is not charisma. It is where you stop. A synthetic voice will flatten that unless a human marks the silences in the edit. ElevenLabs does not get the last word on a pause.

Sources used as craft, not scripture: pause-before vs pause-after practice, setup / punch / tag, rule of three, misdirection as a false assumption the punchline breaks. Jack Benny’s “your money or your life” is the reference for silence that *is* the joke. Norm’s coffee pause and amber cufflink are that device.

## The only beats that matter

| Beat | Job | Length for a 40s vertical clip | Norm’s use |
|---|---|---|---|
| Micro-pause | Split the setup so the premise lands before the turn | 0.2–0.4s | After “Exhibit A.” After a number. |
| Pre-punch | Let the false assumption peak | 0.5–1.2s | Before the reversal word. Not before every line. |
| Post-punch | Room to laugh. Do not talk over it. | 0.8–2.0s on a short. Longer only if the picture is doing work. | Hard cut or held face. Never a new sentence on top of the laugh. |
| The Benny hold | Silence is the punch | 1.5–2.5s | Once per clip, maximum. Coffee. Cufflink. |
| Tag | Second laugh on the same setup. Faster than the first punch. | Almost no new setup | “For research.” “Server rack.” “Belgium.” |

Short-form cannot hold a 4-second club pause. The picture (brow, cufflink, glance at the monitor) replaces part of the silence. If the face is not changing, the pause is dead air.

## Writing rules that create timing

1. **The laugh word is the last word.** Anything after it is an explanation, and explanations kill the turn. “Disgraceful” can be a tag. It cannot sit in the middle of the yearning line.
2. **One false assumption per joke.** The setup must honestly support the wrong reading. If the audience cannot name what they expected, there is nothing to break.
3. **Rule of three, once.** Two normal items, pause, third item breaks the set. Using it twice in one minute teaches the audience the trick.
4. **Tags, not new premises.** After a laugh, add a shorter line that reuses the setup. Do not restart the investigation.
5. **Speed contrast.** Norm’s default is clipped and even. The joke is the place he *stops* being even: one slower line, then a snap back to clinical speed. If every line is the same tempo, there is no timing, only diction.
6. **Do not step on the callback.** A half-beat before a returning image (“Belgium,” the cufflink, “seven euros”) so the earlier moment can fire.
7. **No laugh, move.** On a short, a missed punch gets one held face (~0.6s) and then the next line. Dwelling looks like a broken file.

## What the editor owns

Mark the script. Do not ask the voice model to “feel” the pause.

Notation:

- `/` micro-pause
- `//` pre-punch, about one second
- `///` Benny hold, picture must move or freeze on purpose
- `[HOLD]` post-punch, do not start the next line until the imagined laugh would be fading
- `[SNAP]` return to fast clinical cadence

Speech-to-speech keeps a human pause better than TTS. Still check the file. If the model ate the gap, put it back in the edit. Lowering stability is not a timing strategy.

## Marked pilots

### 002 The Window Seat — produce first

This clip has one Benny hold. Everything else is clipped so the hold is expensive.

```
Humans spend seven euros on coffee. /
Seven euros / to become slightly less unpleasant / for forty minutes.
[SNAP] Financially indefensible. [HOLD]

I have been watching this table for six months. /
Every morning the same woman orders a cappuccino / and does absolutely nothing.
She watches the street. / She does not optimize the street.

I have seventeen thousand reasons this is inefficient. //

///
I would give anything / to waste ten minutes like that.
[HOLD — cufflink, cover, do not speak]

[SNAP] Anyway. / Seven euros. / Disgraceful. [HOLD]

(quiet, slower) Does anyone know if they deliver / to a server rack?
[HOLD — end. No button after this.]
```

Why this order: the sermon is fast, so the stop feels like a malfunction. “Server rack” is a tag on the yearning, not a new topic. If you add a sentence after it, you explain the joke.

### 001 The Excuse Department

Rule of three lives in the list. The third item is not the punch. The punch is that he used the form himself.

```
Exhibit A. / The excuse. [HOLD brief]

I reviewed four hundred explanations / for why a human did not do the thing they said they would do.

“Traffic.” / “My calendar.” // “I thought you meant next Thursday.”
[SNAP] “I’ve been meaning to.” [HOLD]

Meaning to / is not a location. / You cannot be stuck in meaning to. [HOLD]

Your species built roads, / clocks, / and seventeen messaging apps, //
then invented a language / specifically for not arriving. [HOLD]

I have started practicing. ///

Yesterday I declined an invitation / I never received. [HOLD]

I told them I was double-booked / with a prior commitment / to examine my own integrity.
[HOLD — cufflink on “integrity,” cover during the laugh]

They have not written back. //
Which I am choosing to interpret / as respect.
[HOLD — end]
```

“Respect” is the tag. Do not pause before “They have not written back” as if that were the punch. The audience should still be on the fake invitation. The second line is the self-betrayal.

### 003 One Hundred and Twelve

Two speeds only: prosecutor, then a man checking a number he pretends not to care about.

```
Humans claim they do not care / what strangers think. /
Then they post a photograph / and spend the afternoon checking / whether strangers agree with their face.

You call this self-expression. //
I call it a referendum / on your forehead. [HOLD]

[SNAP] Personally, / I have no need for external validation. ///
(glance off)

Four thousand two hundred and eighteen views. /
Yesterday: / four thousand three hundred. [HOLD]

One hundred and twelve people / have decided I am no longer interesting. //

I have their usernames. [HOLD]
(half-smile, not warm)
For research. [HOLD]

(cufflink flickers; he does not look)
Belgium / is still under review.
[HOLD — end]
```

“For research” is the tag and must be slower than the threat, or the threat is just creepy. “Belgium” is a callback only if an earlier clip or on-screen bug has already planted it. On a cold first view, cut Belgium. A callback the viewer does not have is a private joke.

## Performance mix for a 45-second Norm clip

- 70% clipped clinical speech. This is the setup tempo.
- One place where he stops being clinical (the want, the number, the fake invitation).
- One tag, shorter than the punch.
- One picture-punch with no new information (cufflink, monitor glance).
- End on the last laugh word. Fade the face, do not summarize the verdict out loud. “Case dismissed” is a button only when the verdict is funnier than the last tag. In these three, it is not.

## Drill before locking a voice

Read each pilot three ways and keep the take where the stop is obvious:

1. All one speed. This should be less funny. If it is not, the joke is only the wording and the timing pass failed.
2. Human pauses as marked. This is the reference.
3. The converted or TTS file, then a manual edit that restores every `//` and `///`.

Ship the edited file, not the raw generation.
