# Beautiful Handwritten Letters

Letter writing app. User inputs feelings, AI generates a short letter, user can share or send it.

Inspired by *Her* (2013).

---

## Core Flow

1. Landing page with example letter and "create" button
2. Input form: recipient, feeling, one detail
3. AI generates letter
4. Typewriter animation displays letter
5. User can share via link, send via email, or destroy
6. Recipient sees letter with "write your own" button

---

## Sharing

- Unique shareable link per letter
- Email send option
- OG image shows the letter text
- Terms & conditions checkbox before publish

---

## Input Fields

1. Who is this for (name and relationship)
2. What you feel (appreciation, missing them, etc)
3. One specific detail about them

---

## Tech

- Next.js 14
- Vercel
- Claude API
- Vercel KV
- @vercel/og

---

## Timeline

Testing: Jan 27 / Launch: Feb 1

| Days | Task |
|------|------|
| 1-2 | Next.js setup, deploy, input form |
| 3-4 | Claude API, letter generation |
| 5-6 | Typewriter display, share links, database |
| 7-8 | OG image, email, destroy animation |
| 9-10 | Landing page, T&C, mobile |
| 11 | Friend testing, bug fixes |

---

## Success Criteria

- [ ] 100 letters before Feb 14
- [ ] 20%+ sent via email
- [ ] Works on mobile

---

## Open Questions

- Voice input: cut for v1?
- Public library: cut for v1?
