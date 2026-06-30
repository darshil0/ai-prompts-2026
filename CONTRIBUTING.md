# Contributing to AI Prompt Library 2026

Thank you for your interest in contributing! We welcome high-quality prompt submissions and code improvements.

## 📋 Contribution Types

### 1. Adding New Prompts

**Before You Start**
- Review all 200 existing prompts in `index.html` to avoid duplicates
- Ensure your prompt is novel and provides clear value
- Test your prompt in your target AI model

**Submission Steps**

1. **Fork** the repository
2. **Add** your prompt to the `promptData` array in `index.html`:

```javascript
{
  id: 201,                              // Next available ID
  title: "Your Prompt Title",
  category: "Category Name",            // Use existing categories
  description: "Brief one-liner (max 60 characters)",
  tags: ["Tag1", "Tag2"],              // 1-3 relevant tags
  content: "Full prompt text here..."  // Complete, copy-ready prompt
}
```

**Quality Checklist**
- [ ] Prompt has been tested and produces consistent results
- [ ] Title is descriptive (2-4 words)
- [ ] Description is concise and action-oriented
- [ ] Content is well-structured with clear constraints
- [ ] No personal data, API keys, or sensitive information
- [ ] Grammar and formatting are professional
- [ ] Tags align with existing tag vocabulary

3. **Update** category count in README if adding to a new category
4. **Update** CHANGELOG.md with your addition (Unreleased section or draft)
5. **Test** the web interface locally by opening `index.html` in your browser
6. **Submit** a pull request with:
   - Clear title: "Add prompt: [Title]"
   - Description of what the prompt does
   - Category it belongs to
   - Any special AI model requirements

### 2. Improving Existing Prompts

Found an error or way to improve a prompt? Submit a PR with:
- Which prompt ID and title you're updating
- What changed and why
- Testing evidence (screenshots, outputs)

### 3. Code Improvements

Contributions welcome for:
- **Performance**: Optimizing React rendering, reducing bundle size
- **Accessibility**: Improving ARIA labels, keyboard navigation, screen reader support
- **User Experience**: Better search, improved filtering, mobile optimization
- **Design**: Visual refinements, theming, responsive improvements
- **Testing**: Adding test coverage, validation checks

## 🎨 Design & Accessibility Standards

All code contributions must maintain:

**Accessibility**
- Semantic HTML (`<nav>`, `<main>`, `<article>`, etc.)
- ARIA labels on interactive elements (`aria-label`, `aria-expanded`, `aria-pressed`)
- Screen reader-friendly text (`aria-live`, `role="status"`)
- Keyboard navigation support
- Sufficient color contrast (WCAG AA minimum)

**Code Quality**
- Follow existing code style (Prettier-formatted)
- Use meaningful variable names
- Add comments for complex logic
- No console errors or warnings
- Mobile-responsive design

**Performance**
- Lazy-load images where possible
- Minimize external API calls
- Optimize React memoization (avoid unnecessary re-renders)
- Keep bundle size in mind

## 📝 Commit Message Guidelines

```
[type]: [Brief description]

[Optional detailed explanation if needed]
```

**Types**:
- `feat`: New prompt or feature
- `fix`: Bug fix or documentation correction
- `refactor`: Code restructuring without behavior change
- `docs`: Documentation updates
- `perf`: Performance improvement
- `style`: Code formatting or styling

**Examples**:
```
feat: Add prompt 201 - Advanced RAG Pipeline Designer
fix: Correct font names in README from Syne/Outfit to Fraunces/Hanken
docs: Update CHANGELOG for v4.3.0 release
```

## 🔄 Review Process

1. **Initial Review** — We'll check for quality, originality, and adherence to guidelines
2. **Testing** — We'll test your prompt in target AI models and verify browser compatibility
3. **Feedback** — You may receive suggestions for refinement
4. **Merge** — Approved PRs are merged into main
5. **Release** — Your contribution is included in the next version bump and CHANGELOG

## 📊 Category Guidelines

When submitting a prompt, choose the most appropriate category:

| Category | Best For |
|----------|----------|
| **Infographics** | Timelines, flowcharts, visualizations, journey maps |
| **Image Generation** | Photos, artwork, compositions, with grounding/constraints |
| **Image Editing** | Retouching, style transfer, temporal fusion, compositing |
| **Video Generation** | Narrative consistency, camera movements, animations |
| **Marketing** | Social media, ad copy, landing pages, viral content |
| **Career** | Resumes, interviews, LinkedIn, negotiation |
| **Coding** | Full-stack, debugging, algorithms, automation |
| **Problem Solving** | Logic puzzles, reasoning, frameworks, decision-making |
| **Design** | UI/UX, color, typography, accessibility, vibe coding |
| **Agentic AI** | Multi-step workflows, autonomous agents, tool use |
| **Writing & Content** | Ghostwriting, SEO, content strategy, copywriting |
| **Education & Learning** | Tutoring, explanations, quizzes, skill-building |
| **Audio & Music** | Soundscapes, lyrics, podcast processing |
| **Data Analysis** | Dashboards, insight extraction, SQL, visualization |
| **Personal Productivity** | Time management, habit systems, anti-procrastination |

## ⚖️ License

By contributing, you agree that your contributions are licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

## 🤝 Code of Conduct

- Be respectful and constructive
- Provide helpful feedback on PRs
- No harassment, discrimination, or hate speech
- Focus on ideas, not people

## ❓ Questions?

- Check existing [Issues](https://github.com/darshil0/ai-prompts-2026/issues) for FAQs
- Start a [Discussion](https://github.com/darshil0/ai-prompts-2026/discussions)
- Open an Issue with the `question` label

## 🎉 Recognition

Contributors are recognized in:
- CHANGELOG.md (for significant contributions)
- GitHub contributors graph
- README Acknowledgments section (for major contributions)

Thank you for making this prompt library better! 🚀
