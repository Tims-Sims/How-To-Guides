# Simulation QA Testing Checklist

Use this checklist to test any interactive simulation before sign-off. Mark each item as verified. For any failure, record the steps to reproduce it and include a screenshot where useful.

---

## 1. Files and Build Hygiene

- [ ] 1.1 File and folder names follow the project’s naming and folder conventions.
- [ ] 1.2 The simulation contains no temporary, backup, debug, or test files (for example, `.tmp`, `~`, or `test-*` files).
- [ ] 1.3 No commented-out debug code, `console.log` statements, unused assets, dead code, or orphaned files remain.
- [ ] 1.4 The simulation is provided as a single file, with no additional assets required.

## 2. Opening the Simulation and First Screen

- [ ] 2.1 The simulation opens without an error message, blank screen, broken layout, or long loading delay.
- [ ] 2.2 It opens at the intended starting point, not part-way through an activity.
- [ ] 2.3 The simulation title and description are visible and correct.
- [ ] 2.4 The **Begin** button is easy to find and clearly starts the activity.
- [ ] 2.5 A **Read Instructions** option is available on the first screen.
- [ ] 2.6 Instructions appear automatically on a new session and do not interrupt a session already in progress after a page reload.

## 3. Controls and Navigation

- [ ] 3.1 Every visible button works as expected; there are no inactive or no-op buttons.
- [ ] 3.2 **Help/Instructions** opens the instructions from every relevant screen, not only the first screen.
- [ ] 3.3 The **Dark/Light Mode** control switches themes correctly. Its label and icon always show the mode that will be selected next, including on first load.
- [ ] 3.4 The **Fullscreen** control enters and exits fullscreen correctly, including when the user presses Escape.
- [ ] 3.5 The **Review/History** control opens the user’s recorded answers or progress correctly.
- [ ] 3.6 **Reset** asks for confirmation before clearing answers, inputs, and progress.
- [ ] 3.7 Reset keeps the current theme and does not exit fullscreen.
- [ ] 3.8 Any **Play Again**, **Try Again**, or **Restart** control also asks for confirmation before clearing progress.

## 4. Layout and Visual Quality

- [ ] 4.1 The header shows the correct simulation name and all expected controls: Help, theme toggle, fullscreen, Review/History, and Reset.
- [ ] 4.2 Header content is legible and aligned at normal and maximized laptop window sizes.
- [ ] 4.3 Content is not clipped and does not cause unwanted horizontal or vertical scrolling.
- [ ] 4.4 Text is easy to read and has sufficient contrast with its background.
- [ ] 4.5 Buttons and input fields have clear hover and keyboard-focus states.

## 5. Activity Flow and Progress

- [ ] 5.1 Steps appear in a logical order and the user always has a clear next action.
- [ ] 5.2 Progress bars, step counters, and scores accurately reflect the user’s current state and update immediately.

## 6. Answers, Validation, and Feedback

- [ ] 6.1 Correct answers are recognised and scored correctly.
- [ ] 6.2 Incorrect answers are identified correctly and receive useful feedback.
- [ ] 6.3 Validation matches the input type: text fields reject inappropriate numeric-only input, and numeric fields reject text input, with clear guidance for the user.
- [ ] 6.4 Empty or whitespace-only input is treated as empty, not accepted as a valid response.
- [ ] 6.5 Retrying or editing an answer validates it again and does not retain stale results from a previous attempt.
- [ ] 6.6 Scores, labels, and feedback are consistent with one another.
- [ ] 6.7 Unexpected or incorrect input never crashes the simulation; the user receives a clear recovery message.

## 7. Inappropriate-Language Filtering

- [ ] 7.1 A prohibited word in a text answer shows a warning and clears the affected field.
- [ ] 7.2 Only fields containing prohibited language are cleared; clean fields keep their content.
- [ ] 7.3 Whole prohibited words are detected without false positives in harmless words (for example, `assume`).
- [ ] 7.4 Filtering works for mixed case and common number/symbol substitutions (for example, `SwearWord`, `SWEARWORD`, `sw3ar`, and `s.w.e.a.r`).
- [ ] 7.5 If user input is shown again in a review or summary, prohibited language is filtered or flagged and is not shown in shared or exported views.

## 8. Input Limits

- [ ] 8.1 Character limits work when typing, pasting, and using autofill.
- [ ] 8.2 Very long input does not break the layout, saved data, or scoring.

## 9. Stress Testing and Recovery

- [ ] 9.1 Rapid clicking does not create duplicate submissions or history entries, or break the simulation state.
- [ ] 9.2 Rapid clicking **Submit** cannot bypass validation.
- [ ] 9.3 Refreshing the page during a session does not create corrupted or contradictory state.
- [ ] 9.4 Repeatedly opening and closing a modal or dialog does not cause visual glitches or leave the simulation stuck.
- [ ] 9.5 If the simulation uses the internet, losing and restoring the connection does not leave it unusable.

## 10. Accessibility

- [ ] 10.1 The full simulation can be used with a keyboard alone (Tab, Shift+Tab, Enter, Space, and Escape).
- [ ] 10.2 The currently focused button or field is always visually clear.
- [ ] 10.3 Correct/incorrect and pass/fail states use text or icons as well as colour.
- [ ] 10.4 Zooming text with Ctrl/Cmd + `+` does not break the layout.

## 11. Browser Compatibility (Laptop)

- [ ] 11.1 The simulation has been tested in each supported browser (Chrome, Firefox, and Edge, where supported).
- [ ] 11.2 It has been tested in a normal-sized window and a maximized/full window.
- [ ] 11.3 Appearance and behaviour are consistent across supported browsers.

## 12. Performance and Stability

- [ ] 12.1 Typing, clicking, and changing screens feel responsive, with no noticeable lag.
- [ ] 12.2 Animations and transitions are smooth.
- [ ] 12.3 The simulation remains responsive after at least 15 minutes of use.

## 13. Data Handling on Shared Laptops

- [ ] 13.1 Closing the simulation tab or window clears all learner data.

## 14. Content and Copy

- [ ] 14.1 There are no spelling or grammar errors.
- [ ] 14.2 The tone and reading level suit the intended audience.
- [ ] 14.3 No placeholder text remains (for example, “Lorem ipsum”, “TODO”, or “[insert text]”).
- [ ] 14.4 First-time users can understand the instructions without outside help.
- [ ] 14.5 Built-in text, including titles, instructions, feedback, and errors, contains no profanity, slurs, or inappropriate language.
- [ ] 14.6 Examples, sample data, and placeholder names are appropriate for the intended audience.

## 15. Debugging for Testing

- [ ] 15.1 Any bugs found are included in detail below, with steps to reproduce, the expected result, and the actual output.

### Bug Report Details

For each bug found, record:

- **Bug description:**
- **Steps to reproduce:**
- **Expected result:**
- **Actual output:**
