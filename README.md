# Hyperwolf — Swap & Upsell engine demo

**→ https://dev-hyperwolf.github.io/commerce-demo/**

A runnable demo of the cart swap and upsell logic for the new hyperwolf.com.
Two flows on one page, both driven by the real engine rather than mocked up:

- **Cart & checkout** — the customer swaps their own basket. A swap replaces a
  *product*; the fulfilment lane only constrains which alternatives are eligible.
- **Driver app & support** — the order is already out with a driver. This one is
  an upsell flow, the candidate pool is a single van, and breaking a promotion
  the customer already earned will not commit until it is acknowledged.

Move the sliders on the right and the cart re-renders from the engine. The
panel underneath shows the reasoning: lane stock, promotion progress, and why
each swap tab returned what it did.

---

## This is a mirror, not a source

Everything here is generated. The engine, its tests and its documentation live
in **`dev-hyperwolf/hyperwolf-commerce-logic`** (private).

```
npm run demo    # rebuilds demo/standalone.html
```

Then copy that file over `index.html` here. The build asserts the page still
renders currency correctly before it writes anything, and a DOM test suite
drives this exact file by clicking through both flows.

**Do not edit `index.html` by hand.** It is a build artifact and the next
regeneration will overwrite it.
