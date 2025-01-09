# Writing Test Specifications

## Unit Tests

### //1: Function `multiplication`

A function called `multiplication` that returns the product of two input numbers.

#### Expect:

- `multiplication(2, 3)` to return a number.
- `multiplication(2, -3)` to return a negative number.
- `multiplication(2, 2)` to return an even number.
- `multiplication(2, 3)` to return `6`.
- `multiplication("a", 3)` to throw an error.
- `multiplication(4, 5)` to return `20`.
- `multiplication(0, 5)` to return `0`.
- `multiplication(3, undefined)` to throw an error

---

### //2: Function `concatOdds`

A function called `concatOdds` takes two arrays of integers as arguments. It should return a single array containing only the odd numbers, in ascending order, from both arrays.

#### Expect:

- `concatOdds([3, 2, 1], [9, 1, 1, 1, 4, 15, -1])` to return `[-1, 1, 3, 9, 15]` (provided example).
- `concatOdds([], [7, 9])` to return `[7, 9]`.
- `concatOdds(["a", "b", "c"], [1, 2, 3, 4, 6, 13])` to throw an error.
- `concatOdds([2, 2, 4, 8], [10, 12, 14, 18])` to return `[]`.
- `concatOdds([], [])` to return an empty array `[]`.
- `concatOdds([1, 2, 3])` to return an error (missing the second array).

---

## Functional Tests

### Shopping Cart Checkout

A feature allowing a user to check out as either a guest (without an account) or a logged-in user. Users should be asked if they want to create an account or log in if checking out as a guest.

#### Expected Behavior:

- **Guest Checkout:**

  - If a customer chooses to check out as a guest, they will be prompted with four popups asking if they want to create an account.
  - Declining to create an account will display a judgmental face and a sad puppy.
  - Guest receipts will indicate the company's disappointment with the customer's choice.

- **Member Checkout:**
  - Customers who select that they have an account will be prompted to enter id info.
  - Customers will be presented with multiple id options (e.g., email, phone).
  - A user interface (similar to a Target self-checkout I guess) will appear for ID input.
  - A keyboard option should be available for manual input.
  - Once entries are logged, a button (potentially animated or glowing or moving around the screen rapidly making it difficult to press in order to make the experience more like a video game)
    will allow progression to the next step.

#### Specific Edge Cases:

- **Forgotten Accounts:**

  - Customers attempting to create an account despite already having one will be informed of their error and must resolve it (figure out the correct email and password).

- **Forgotten Information:**

  - Users forgetting their account information will trigger a loud and terrifying alert and/or a popup saying: "Uh oh, you are silly!".

- **Interference:**

  - If a toddler presses all buttons simultaneously, a popup will request: "Please control your child."

- **Damage:**
  - Smashing the checkout machine results in free items, but only as a guest.
