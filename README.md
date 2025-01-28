# Next.js 15 Counter Update Issue

This repository demonstrates a problem with real-time UI updates in a Next.js 15 application.  A simple counter on the About page lags behind the actual counter value. 

## Bug Description
The counter increments every second, but the display on the About page is not updated immediately, resulting in a noticeable delay. This effect is more pronounced on larger updates or when switching between pages frequently.

## Reproduction Steps
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server.
4. Navigate to `/about`.
5. Observe the counter.  The displayed counter value will lag behind the actual value.

## Solution
The solution involves using `useLayoutEffect` instead of `useEffect`.  `useLayoutEffect` ensures that the updates are applied before the browser performs layout, providing the instant synchronization needed.

## License
MIT