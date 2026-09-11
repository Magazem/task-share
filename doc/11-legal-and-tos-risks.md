# Legal and Terms-of-Service Risks

> This is a product-risk map, not legal advice. A real launch should
> receive jurisdiction-specific legal review.

## AI provider terms

The original concept included letting strangers use another person’s
paid Codex or Claude subscription through an automated bridge.

That should **not** be the product assumption.

OpenAI’s current service terms govern use of its services, and Codex
usage can be governed by the applicable ChatGPT or service agreement
depending on the account/product.\[^1\]\[^2\]

The safe product posture is:

> Each contributor uses an AI product under their own authorization and
> responsibility.

## Account sharing

Avoid:

- pooling consumer subscriptions;
- credential sharing;
- proxying one account to many strangers;
- hidden automated use of a personal account.

If provider-specific integrations are ever added, obtain explicit
legal/terms review.

## Credits

Credits create several questions:

- Are credits transferable?
- Can they be purchased?
- Can they be redeemed for money?
- Can they expire?
- Are they promotional points or consideration for services?
- What happens on account closure?
- Are partner rewards taxable?

Keeping credits non-cash and ecosystem-specific initially reduces
complexity, but does not eliminate it.

## Marketplace worker classification

If the platform eventually handles paid work, worker classification can
become relevant depending on jurisdiction and operating model.

A credit-only system does not automatically eliminate employment or
contractor questions.

## Intellectual property

Tasks need clear terms covering:

- ownership of submitted code;
- license of contributions;
- third-party dependencies;
- AI-generated code;
- contributor warranties;
- open-source license compatibility.

For open-source work, the task should inherit or explicitly respect the
repository’s license and contribution rules.

## Confidentiality

Private repository tasks may require:

- confidentiality terms;
- data processing agreements;
- access controls;
- deletion policies;
- audit logs.

## Security liability

If the platform enables third-party contributors to modify private code,
security incidents may create substantial liability.

This is another reason to begin with public repositories.

## Recommended legal sequence

### Phase 1

Public/open-source only.

### Phase 2

Private projects with explicit contributor terms.

### Phase 3

Business/enterprise agreements.

### Phase 4

Potential cash economy after specialized financial/legal review.

## Key rule

Never market the system as a way to bypass or work around AI-provider
restrictions. The platform should be designed to operate within the
permissions and terms applicable to each contributor’s tools.
