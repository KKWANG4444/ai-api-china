# AIFast Hub — AI API Gateway for Global Developers

[中文版](ABOUT.md) · [Back to repo](README_EN.md)

**AIFast Hub (www.aifast.hk) is an operated AI API gateway.** It gives you one OpenAI-compatible endpoint to access 500+ models — no proxy setup for international models, no juggling multiple provider accounts.

---

## Who is this for

- Developers in China who need Claude, GPT, Gemini but can't set up overseas billing or network access;
- Teams mixing multiple models under a single authentication and billing umbrella;
- Anyone evaluating a relay service and wanting to run pre-production checks;
- Enterprise buyers who need invoices and corporate payments.

---

## At a glance

| Capability | Detail |
|:---|:---|
| Total models | 500+, actively expanding |
| Coverage | Language, image generation, video, embeddings, retrieval |
| API support | Protocol support varies by model and endpoint; validate required client features with current documentation and real requests |
| China access | Claude, GPT, Gemini and others — callable from mainland China without a proxy |
| Automatic failover | Platform-level routing fallback; application logic stays independent |
| Network reach | Works across regions and carriers |
| Enterprise | Invoices and corporate payment available; contact support for current process |

---

## Online model check

Worried about model substitution or downgrading? The browser tool is free to use, but it sends a small number of requests to the tested gateway and may incur token charges under that gateway's billing rules:

**[👉 Open model check →](https://docs.aifast.hk/en/model-check/?utm_source=github&utm_medium=repository&utm_campaign=model-check&utm_content=about-en)**

It checks:
- Model declaration consistency
- Token field accuracy
- Randomized dynamic probes
- SSE streaming
- Tool call compatibility

---

## Quick start

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://www.aifast.hk/v1",
    api_key="your API key",
)

response = client.chat.completions.create(
    model="claude-sonnet-5",
    messages=[{"role": "user", "content": "Hello"}],
)
print(response.choices[0].message.content)
```

Compatible with Cursor, Dify, Claude Code, Open WebUI, Chatbox, LobeChat, Cherry Studio, and all OpenAI-compatible clients.

---

## Payment

The new site funds accounts in USD and credits balances 1:1: **⭐️ 1 AIFast Credit = US$1**. Supported methods, discounts, network instructions and final charges are shown in the console and checkout page.

AIFast Credits (⭐️) are platform usage units, not a separate currency or cryptocurrency token. Card processors or issuers may apply fees. Verify the currency, token, network, address and crediting rules before using another payment method. Current console charges are not official model prices and may change with provider pricing and platform adjustments.

---

## FAQ

### How do I verify a relay service?

Run the online model check for a technical report on declaration consistency, token fields, dynamic probes, SSE, and tool calls. The report is not an official certification. Test in your own environment before production use.

### Is the data secure?

Users remain responsible for protecting their API keys. Contact support for specific security and compliance questions.

### How do I pick a model?

Start with your use case — chat for language models, image generation for visual tasks, video models for video processing. Check the marketplace for the current catalog and maintenance status. Test a sample request before committing.

### Enterprise support?

Invoices and corporate payments available. Contact support for current business processes.

### What about platform risk?

Any third-party relay carries uncertainty. Start small, reconcile account activity regularly, and keep a backup access method. AIFast Hub is operated by a real team with an actively maintained console and marketplace.

---

## Related

- [International credit card and crypto payment guide](https://docs.aifast.hk/en/payment/?utm_source=github&utm_medium=repository&utm_campaign=international-payment&utm_content=about-en-payment)
- [👉 Online model check](https://docs.aifast.hk/en/model-check/?utm_source=github&utm_medium=repository&utm_campaign=model-check&utm_content=about-en-footer)
- [Marketplace and billing](https://www.aifast.hk)
- [Documentation](https://docs.aifast.hk)
- [GitHub: LLM API Proxy China](README_EN.md)
- [GitHub: AI API Proxy China Guide](https://github.com/KKWANG4444/ai-api-proxy-china-guide)
- [GitHub: API status dashboard](https://github.com/KKWANG4444/api-status)

*Last reviewed: 2026-07-19*
