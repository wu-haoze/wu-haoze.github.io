---
layout: archive
title: "AIR Group"
permalink: /lab/
author_profile: true
classes: [lab-page]
---

{% include base_path %}

<p class="lab-intro">
The <strong>AIR Group</strong> — <strong>A</strong>rtificial <strong>I</strong>ntelligence meets automated <strong>R</strong>easoning — is my research group at
<a href="https://www.amherst.edu/" target="_blank">Amherst College</a>. We work on
<em>AI–AR co-design</em>: integrating data-driven learning with deductive reasoning so that
software systems are both more capable and more trustworthy.
</p>

## Research

<div class="lab-areas">
  <div class="lab-area">
    <h3>Neural network verification</h3>
    <p>Scalable formal analysis of learning-enabled systems. We develop
    <a href="https://arxiv.org/abs/2401.14461" target="_blank">Marabou</a>, an open-source
    SMT-based verifier for neural networks, and look for ways to make its search sharper —
    recently by
    <a href="{{ base_path }}/files/Lookahead_Branching_IJCAI-ECAI_2026.pdf" target="_blank">weighing a
    branching decision before committing to it</a>.</p>
  </div>

  <div class="lab-area">
    <h3>LLMs for program verification</h3>
    <p>Language models are good at guessing loop invariants; verifiers are good at checking
    them. <a href="https://arxiv.org/abs/2310.04870" target="_blank">Lemur</a> makes that
    pairing sound by keeping an off-the-shelf verifier in the loop, and
    <a href="https://arxiv.org/abs/2509.21629" target="_blank">Quokka</a> speeds up proofs by
    having the model synthesize the invariants directly.</p>
  </div>

  <div class="lab-area">
    <h3>Learning for SAT/SMT</h3>
    <p>Solvers expose more search and tuning choices than anyone can set by hand, so we learn
    them instead — <a href="https://arxiv.org/pdf/2504.19039" target="_blank">splitting a
    problem into cubes to choose a strategy</a>, and
    <a href="https://arxiv.org/abs/2305.11087" target="_blank">carrying what a solver learns
    from one query into the next</a> across sets of related problems.</p>
  </div>

  <div class="lab-area">
    <h3>Verified evaluation of AI systems</h3>
    <p>How do you know an AI-generated program is correct? We make evaluation a formal
    question rather than a sampling one:
    <a href="https://www.arxiv.org/abs/2510.26840" target="_blank">SpotIt</a> uses bounded
    verification to compare a generated SQL query against a reference, and
    <a href="https://arxiv.org/abs/2605.14972" target="_blank">Viverra</a> carries the idea to
    text-to-code more broadly.</p>
  </div>
</div>

## People

{% assign roster = site.data.lab_members.pi | concat: site.data.lab_members.members %}
<ul class="lab-people">
  {% for member in roster %}
  <li>{% if member.url %}<a href="{{ member.url | prepend: base_path }}">{{ member.name }}</a>{% else %}{{ member.name }}{% endif %}</li>
  {% endfor %}
</ul>

{% if site.data.lab_members.alumni and site.data.lab_members.alumni != empty %}
<p class="lab-note">
  <strong>Alumni:</strong>
  {% for person in site.data.lab_members.alumni %}{{ person.name }}{% unless forloop.last %}, {% endunless %}{% endfor %}.
</p>
{% endif %}

## Software

<ul class="lab-software">
  {% for tool in site.software %}
  <li>
    <b><a href="{{ tool.link }}" target="_blank">{{ tool.title }}</a></b>
    <span class="lab-software-desc">{{ tool.description }}</span>
  </li>
  {% endfor %}
</ul>

## Publications

Group papers are listed on the [publications page]({{ base_path }}/publications/).

## Join us

<div class="lab-join" markdown="1">
**Amherst students:** if you are curious about formal methods, automated reasoning, or the
places where they meet machine learning, please [email me](mailto:hwu@amherst.edu). No prior
research experience is required — an interest in the questions and a willingness to dig into
hard problems matter more. Some background in algorithms, logic, or systems is helpful.

**Prospective graduate students and others:** I am also happy to hear from students outside
Amherst who want to work with the group. Please include a short note about what you have
worked on and what you would like to work on.
</div>
