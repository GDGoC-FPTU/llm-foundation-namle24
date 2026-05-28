# Day 1 Exercises and Reflection
## LLM API Foundation Practice

Duration: 1:30 hours
Structure: Core coding (60 minutes) then extension exercises (30 minutes)

## Part 1 — Core Coding (0:00 to 1:00)

Run the Colab examples at: https://colab.research.google.com/drive/172zCiXpLr1FEXMRCAbmZoqTrKiSkUERm?usp=sharing

Implement every TODO in `template.py`. Use `pytest tests/` to check progress.

Check point: after completing the first 4 tasks, run:

```bash
python template.py
```

You should see comparison output for GPT-4o and GPT-4o-mini.

## Part 2 — Extension Exercises (1:00 to 1:30)

### Exercise 2.1 — Temperature Sensitivity
Call `call_openai` with temperature values 0.0, 0.5, 1.0, and 1.5 using the prompt "Tell me one interesting fact about Vietnam."

What pattern do you notice across the four responses? (2 to 3 sentences)
> When temperature is low, responses are more focused, direct, and repeatable. Higher temperature values produce more creative and varied answers, with more detail and less strict wording.

What temperature would you choose for a customer support chatbot, and why?
> I would use a low temperature like 0.0 to 0.2 so the bot stays consistent, accurate, and avoids unnecessary or risky creativity.

### Exercise 2.2 — Cost Tradeoff
Consider this scenario: 10,000 active users per day, each making 3 API calls, and each call averages 350 tokens.

Estimate how many times more expensive GPT-4o is than GPT-4o-mini for this workload.
> GPT-4o is roughly 30 to 35 times more expensive than GPT-4o-mini for the same token volume.

Describe one case where the higher cost of GPT-4o is worth it, and one case where GPT-4o-mini is the better choice.
> GPT-4o is worth it for complex analysis, high-quality content creation, or critical use cases with strong accuracy needs. GPT-4o-mini is better for high-volume FAQ handling, simple automation, and cost-sensitive applications.

### Exercise 2.3 — User Experience with Streaming
When is streaming most important, and when is non-streaming more appropriate? (one paragraph)
> Streaming is most important for real-time chat and long responses, because it gives the user immediate feedback and reduces perceived delay. Non-streaming is more appropriate for short answers, batch jobs, or cases where the final result can be shown only after all processing is complete.

## Submission Checklist
- [ ] All tests pass: `pytest tests/ -v`
- [ ] `call_openai` implemented and verified
- [ ] `call_openai_mini` implemented and verified
- [ ] `compare_models` implemented and verified
- [ ] `streaming_chatbot` implemented and verified
- [ ] `retry_with_backoff` implemented and verified
- [ ] `batch_compare` implemented and verified
- [ ] `format_comparison_table` implemented and verified
- [ ] `exercises.md` completed in English
- [ ] Copy your work to the `solution` folder as required
