<div align="center">

![](https://img.shields.io/badge/Conference_Corral-Attendee_Intelligence-7B2FBE?style=for-the-badge)
![](https://img.shields.io/badge/Know_Your_Room-Before_You_Walk_In-F5A623?style=for-the-badge)

# Conference Corral

### Build a profile on every person in the room before you say hello.

Walk into any event knowing who's there, what they do, and exactly how to open a conversation with them.

</div>

---

## What This Is

Conference Corral is a repeatable process for turning an attendee list into actionable profiles. Give it a spreadsheet of names and emails. Get back a full dossier: roles, LinkedIn links, background, intro angles, flags, and a room expertise map.

Built for workshop facilitators, event organizers, sales teams, and anyone who wants to show up prepared instead of winging it.

---

## What You Get

For each attendee:
- **Role and company** - what they actually do, not just their job title
- **LinkedIn and public links** - verified, not guessed
- **Confidence level** - HIGH / MEDIUM / LOW so you know what to trust
- **Intro angle** - one sentence on how to open a conversation with them
- **Setup context** - relevant details from the registration form
- **Flags** - anything worth knowing before the event (typos, no-shows, unusual situations)

Plus a **room expertise map** that groups everyone by skill tier so you can see the shape of your audience at a glance.

---

## How to Use It

### 1. Collect your attendee data

You need at minimum: name and email. The more you have from your registration form, the richer the profiles.

Useful fields to collect:
- Full name
- Email
- Job title / company (if you ask)
- What tools or experience they have (relevant to your event)
- Computer / setup (for workshops)

### 2. Run the research prompt

Open Claude and paste this prompt with your attendee list:

```
I'm running a [type of event] called [name] on [date] in [location].

I have [N] attendees and I want to build a profile on each one for introductions and facilitation purposes.

For each person, search LinkedIn, Google, and any other public sources. Return:
- Full name
- Likely job title and company
- LinkedIn URL if found
- Any other relevant public info (GitHub, Twitter, portfolio, notable projects)
- Confidence level: HIGH (multiple verified sources), MEDIUM (one source or strong inference), LOW (no public profile found)
- One-sentence intro angle - how to open a conversation with this person

Here is my attendee list:
[paste your list]
```

### 3. Compile into profile cards

Use the template in `templates/profile-card.md` for each person.

Use the template in `templates/profiles-full.md` for the complete document.

### 4. Add your flags and room map

After compiling profiles, add:
- A flags table for anything that needs action before the event
- A room expertise map grouping attendees by skill/background tier

See `examples/stellarph-workshop-2026.md` for a real example.

---

## What to Do With Profiles

**Before the event:**
- Brief your co-facilitators so everyone knows who's in the room
- Identify who can be peer resources (people who can help others get unstuck)
- Spot the beginners who'll need extra support
- Action any flags (wrong emails, attendance confirmations, etc.)

**During the event:**
- Use intro angles to open conversations naturally
- Pair experienced and new attendees intentionally
- Know which pods or groups have the right balance of skills

**After the event:**
- Use LinkedIn links for follow-up outreach
- Reference background in your follow-up message to make it personal

---

## Repo Structure

```
conference-corral/
├── README.md               - this file
├── templates/
│   ├── profile-card.md     - single person template
│   └── profiles-full.md    - full event profiles document template
├── prompts/
│   └── research-prompt.md  - the Claude prompt to run research
└── examples/
    └── stellarph-workshop-2026.md  - real profiles from the StellarPH Claude AI Workshop
```

---

## Tips and Edge Cases

**Gmail addresses give no company info** - you're searching by name only. Results vary.

**Work email domains are free intel** - `name@company.com` tells you the employer before you search anything.

**Common names are hard** - in the Philippines, names like Christian Delos Santos or Mark Garcia will return many results. Use location + context to narrow.

**Some people have no public footprint** - this is normal. Early-career, private-profile, or non-English-indexed professionals often don't show up. Flag as LOW and ask them directly at the event.

**Email patterns reveal age** - handles like `name071206` often encode a birthdate (07/12/2006). Useful for gauging experience level.

**First-name-only registrations** - some events collect incomplete data. No last name = no search possible. Flag these and watch for them during check-in.

---

<div align="center">

Built by ARC | Advertising Report Card

*Know your room before you walk in.*

</div>
