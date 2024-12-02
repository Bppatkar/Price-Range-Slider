# Price-Range-Slider

This project implements a **price range selector** using HTML, CSS, and JavaScript. The feature includes synchronized input boxes and range sliders to allow users to set a minimum and maximum price while adhering to constraints such as a minimum price gap and valid ranges.

## Features

- **Two-way synchronization**: Adjusting the input boxes updates the sliders, and vice versa.
- **Validation**:
  - Minimum price cannot be less than `0`.
  - Maximum price cannot exceed `10,000`.
  - A fixed price gap (`priceGap`) is enforced between the minimum and maximum values.
- **Dynamic visual feedback**:
  - The progress bar between the slider thumbs updates dynamically to reflect the selected range.

## Usage

### 1. Input Elements
- Two **input boxes** for minimum and maximum prices.
- Two **range sliders** for selecting minimum and maximum prices.

### 2. Dynamic Validation
- Enforces valid ranges:
  - Minimum price is clamped to `0` or higher.
  - Maximum price is clamped to `10,000` or lower.
- Maintains a minimum gap (`priceGap`) between the selected minimum and maximum prices.

### 3. User Interactions
- **Input Boxes**:
  - Users can manually type in the desired price values.
  - If the entered value violates constraints, it is automatically adjusted.
- **Range Sliders**:
  - Users can drag the thumbs of the sliders to set price values.
  - Adjustments are synchronized with the input boxes.

## Code Overview

### Key Components

1. **Input Elements**
   - `.price-input input`: Input boxes for the minimum and maximum price values.
   - `.range-input`: Range sliders for setting the price range.

2. **Event Listeners**
   - Input box changes (`input` event): Updates the sliders and enforces constraints.
   - Slider changes (`input` event): Updates the input boxes and enforces constraints.

3. **Validation Logic**
   - Ensures prices remain within valid bounds (`0 to 10,000`).
   - Enforces a minimum price gap (`priceGap`) between the minimum and maximum values.

4. **Dynamic Styling**
   - Updates the slider progress bar dynamically using `style.left` and `style.right`.


