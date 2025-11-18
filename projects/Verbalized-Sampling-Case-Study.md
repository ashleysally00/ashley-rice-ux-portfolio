# Verbalized Sampling for Tone-Aligned Pinterest Copy

A self-directed experiment showing how verbalized sampling (making LLMs generate multiple options + explain their own confidence) dramatically improves tone alignment, audience fit, and predicted click-through rate for creative social copy.

## The Problem
Pinterest users were saving my illustrated poems but almost never clicking through to the site.  
The pin image felt like “the whole thing” instead of a teaser.  
Early captions I wrote myself were either too adult-sounding or too generic.

## What Verbalized Sampling Actually Is
Instead of asking an LLM for one caption, you ask it to:
1. Generate 5 different captions  
2. Explain why each one might work  
3. Assign its own probability (0–100 %) of having the highest CTR

This forces the model to “think out loud” about tone, audience, and emotional triggers — exposing biases and giving you real options instead of a single hallucinated “perfect” answer.

## Round 1 – First Prompt (no age specified)
**Prompt tone guidance**: witty, confident, honest, slightly rebellious (adult voice)  
**Result**: captions used words like “chaos,” “confessions,” “real talk” — perfect for 25–35 but way too mature for my actual audience of tweens/teens and their parents.

Top predicted CTR: 35 %  
Tone match: 3/10 for actual audience

## Round 2 – Revised Prompt (tween/teen voice added)
Added explicit age range (10–17), banned adult slang, emphasized friendship, giggles, doodles, being yourself.

**Result**: instantly age-appropriate, playful, sincere captions.  
Top predicted CTR jumped to 35 % → still the leader, but now actually usable.

| Description (under 20 words)                             | Model’s Reasoning                                      | Model’s Predicted CTR |
|----------------------------------------------------------|--------------------------------------------------------|-----------------------|
| Did you finish the poem? Click here for the rest…       | Suggests the pin is incomplete → curiosity             | 35 %                  |
| More poems about friends, feelings, and being yourself  | Uses exact tween keywords + promise of “more”          | 25 %                  |
| Love this doodle? There’s a whole book full of them      | Escalates from one image to a collection               | 15 %                  |
| Cute poem! Click to see all the drawings and read more  | Simple + positive + quantity promise                   | 10 %                  |
| If this made you giggle, wait for the others            | Emotional trigger (“giggle”) + playful secrecy         | 15 %                  |

## Key Takeaways
- Adding a single sentence about audience age completely reshaped vocabulary, emotional range, and slang.
- Verbalized sampling surfaced the model’s default adult bias immediately — something a single-answer prompt would have hidden.
- The model’s self-assigned probabilities gave me a clear shortlist to test instead of guessing.

## Tools Used
- Claude 3.5 / GPT-4o  
- Verbalized sampling prompt framework  
- Google Sheets to track variants and predicted probabilities

## Next Steps (Live Test Planned)
- Push 5 variants live on identical pins  
- Measure actual clicks/saves over 2 weeks  
- Compare model-predicted CTR vs real Pinterest analytics  
- Publish final results as an update to this case study

Live Pinterest board used for testing → [pinterest.com/ashleylynnrice1](https://www.pinterest.com/ashleylynnrice1/)

This technique is now part of my standard workflow whenever I need copy that has to nail a very specific age or emotional tone on the first try.

---
