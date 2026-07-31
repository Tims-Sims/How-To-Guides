# Simulation QA Testing Checklist

Use this checklist to test any interactive simulation before sign-off. Mark each item as verified. For any failure, record the steps to reproduce it and include a screenshot where useful.

---

## 1. Commit and Version Control

- [ ] The commit message includes the correct issue or ticket number.
- [ ] The commit contains only changes related to that issue; no unrelated work is included.

## 2. Files and Build Hygiene

- [ ] File and folder names follow the project’s naming and folder conventions.
- [ ] The simulation contains no temporary, backup, debug, or test files (for example, `.tmp`, `~`, or `test-*` files).
- [ ] No commented-out debug code, `console.log` statements, unused assets, dead code, or orphaned files remain.
- [ ] The simulation is provided as a single file, with no additional assets required.

## 3. Opening the Simulation and First Screen

- [ ] The simulation opens without an error message, blank screen, broken layout, or long loading delay.
- [ ] It opens at the intended starting point, not part-way through an activity.
- [ ] The simulation title and description are visible and correct.
- [ ] The **Begin** button is easy to find and clearly starts the activity.
- [ ] A **Read Instructions** option is available on the first screen.
- [ ] Instructions appear automatically on a new session and do not interrupt a session already in progress after a page reload.

## 4. Controls and Navigation

- [ ] Every visible button works as expected; there are no inactive or no-op buttons.
- [ ] **Help/Instructions** opens the instructions from every relevant screen, not only the first screen.
- [ ] The **Dark/Light Mode** control switches themes correctly. Its label and icon always show the mode that will be selected next, including on first load.
- [ ] The **Fullscreen** control enters and exits fullscreen correctly, including when the user presses Escape.
- [ ] The **Review/History** control opens the user’s recorded answers or progress correctly.
- [ ] **Reset** asks for confirmation before clearing answers, inputs, and progress.
- [ ] Reset keeps the current theme and does not exit fullscreen.
- [ ] Any **Play Again**, **Try Again**, or **Restart** control also asks for confirmation before clearing progress.

## 5. Layout and Visual Quality

- [ ] The header shows the correct simulation name and all expected controls: Help, theme toggle, fullscreen, Review/History, and Reset.
- [ ] Header content is legible and aligned at normal and maximized laptop window sizes.
- [ ] Content is not clipped and does not cause unwanted horizontal or vertical scrolling.
- [ ] Text is easy to read and has sufficient contrast with its background.
- [ ] Buttons and input fields have clear hover and keyboard-focus states.

## 6. Activity Flow and Progress

- [ ] Steps appear in a logical order and the user always has a clear next action.
- [ ] Progress bars, step counters, and scores accurately reflect the user’s current state and update immediately.

## 7. Answers, Validation, and Feedback

- [ ] Correct answers are recognised and scored correctly.
- [ ] Incorrect answers are identified correctly and receive useful feedback.
- [ ] Validation matches the input type: text fields reject inappropriate numeric-only input, and numeric fields reject text input, with clear guidance for the user.
- [ ] Empty or whitespace-only input is treated as empty, not accepted as a valid response.
- [ ] Retrying or editing an answer validates it again and does not retain stale results from a previous attempt.
- [ ] Scores, labels, and feedback are consistent with one another.
- [ ] Unexpected or incorrect input never crashes the simulation; the user receives a clear recovery message.

### Inappropriate-language filtering

- [ ] A prohibited word in a text answer shows a warning and clears the affected field.
- [ ] Only fields containing prohibited language are cleared; clean fields keep their content.
- [ ] Whole prohibited words are detected without false positives in harmless words (for example, `assume`).
- [ ] Filtering works for mixed case and common number/symbol substitutions (for example, `SwearWord`, `SWEARWORD`, `sw3ar`, and `s.w.e.a.r`).
- [ ] If user input is shown again in a review or summary, prohibited language is filtered or flagged and is not shown in shared or exported views.

## 8. Input Limits

- [ ] Character limits work when typing, pasting, and using autofill.
- [ ] Very long input does not break the layout, saved data, or scoring.

## 9. Stress Testing and Recovery

- [ ] Rapid clicking does not create duplicate submissions or history entries, or break the simulation state.
- [ ] Rapid clicking **Submit** cannot bypass validation.
- [ ] Refreshing the page during a session does not create corrupted or contradictory state.
- [ ] Repeatedly opening and closing a modal or dialog does not cause visual glitches or leave the simulation stuck.
- [ ] If the simulation uses the internet, losing and restoring the connection does not leave it unusable.

## 10. Accessibility

- [ ] The full simulation can be used with a keyboard alone (Tab, Shift+Tab, Enter, Space, and Escape).
- [ ] The currently focused button or field is always visually clear.
- [ ] Correct/incorrect and pass/fail states use text or icons as well as colour.
- [ ] Zooming text with Ctrl/Cmd + `+` does not break the layout.

## 11. Browser Compatibility (Laptop)

- [ ] The simulation has been tested in each supported browser (Chrome, Firefox, and Edge, where supported).
- [ ] It has been tested in a normal-sized window and a maximized/full window.
- [ ] Appearance and behaviour are consistent across supported browsers.

## 12. Performance and Stability

- [ ] Typing, clicking, and changing screens feel responsive, with no noticeable lag.
- [ ] Animations and transitions are smooth.
- [ ] The simulation remains responsive after at least 15 minutes of use.

## 13. Data Handling on Shared Laptops

- [ ] Closing the simulation tab or window clears all learner data.

## 14. Content and Copy

- [ ] There are no spelling or grammar errors.
- [ ] The tone and reading level suit the intended audience.
- [ ] No placeholder text remains (for example, “Lorem ipsum”, “TODO”, or “[insert text]”).
- [ ] First-time users can understand the instructions without outside help.
- [ ] Built-in text, including titles, instructions, feedback, and errors, contains no profanity, slurs, or inappropriate language.
- [ ] Examples, sample data, and placeholder names are appropriate for the intended audience.
