# AGENTS.md

## General Workflow

- After completing any code modification, always run `pnpm lint` as the final step.
- Preferably, run pnpm lint after the user clicks Keep to confirm changes.

---

## Tailwind & `cn` Usage Rules

### Core Rules

1. **Both layout and non-layout classes:**

   * Must use `cn`
   * Must split into **two lines**
   * **First line:** layout classes (e.g., `flex`, `grid`, `items-center`)
   * **Second line:** non-layout classes (e.g., spacing, colors, typography)

   **Example:**

   ```vue
   :class="cn(
     'flex flex-col h-full',
     'space-y-6 bg-slate-50',
   )"
   ```

2. **Only non-layout classes:**

   * Use a **single `class` attribute**
   * No need for `cn`

   **Example:**

   ```vue
   class="bg-white p-6 rounded-lg border border-slate-100 shadow-sm"
   ```

3. **Only layout classes:**

   * Use a **single `class` attribute**
   * No need for `cn`

   **Example:**

   ```vue
   class="flex space-x-3"
   ```

* **If a component has both layout and non-layout Tailwind classes, use `cn` and split into two lines (layout classes first).**
* **If a component has only layout classes or only non-layout classes, use a single `class` attribute without `cn`.**
