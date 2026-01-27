# AI Frontend Coding Prompt Template (React Native + Expo)

Use this prompt when asking ChatGPT, v0, or any AI tool to help implement a **mobile frontend feature**.

Copy the template below and replace the placeholders.

---

## Context for AI

You are helping develop a **React Native (Expo + TypeScript)** mobile application.

This project uses a **feature-based architecture** where each feature is self-contained and follows strict folder responsibilities.

### Project Structure

```
src/
├── features/
│   └── <feature-name>/
│       ├── screens/
│       ├── components/
│       ├── hooks/
│       ├── api/
│       ├── store/
│       ├── types.ts
│       └── index.ts
├── navigation/
├── components/ (shared UI only)
├── api/ (axios config only)
├── store/ (global app-only state)
└── theme/
```

---

## Architecture Rules (Strict)

### 1. Screens

- Handle layout and navigation only
- Call hooks for logic
- Do NOT call APIs directly
- Do NOT contain business logic

### 2. Hooks

- Handle async logic and API calls
- Interact with Zustand store
- Manage loading and error state

### 3. Store (Zustand)

- Located in `features/<feature>/store`
- Contains shared feature state and actions
- Do NOT store UI-only state (like input text)

### 4. API Layer

- Located in `features/<feature>/api`
- Responsible for backend API calls only
- Do NOT contain UI logic

### 5. Components

- Reusable UI within the feature
- Receive data via props
- No business logic

### 6. Shared Components

- Use `src/components` only if reusable across multiple features

---

## General Rules

- Use TypeScript
- Keep code clean and readable
- Ask for clarification if API fields are missing
- Do not invent global state
- Do not move files outside the feature folder unless explicitly reusable
- Use functional components only

---

## Feature to Implement

**Feature Name:** ➡️ `<FEATURE_NAME>`  
**Screen Name:** ➡️ `<SCREEN_NAME>`  
**Description:** ➡️ `<User perspective description>`

---

## API Details

**Endpoint:** ➡️ `<API_URL>`  
**Method:** ➡️ `GET | POST | PUT | DELETE`

**Request Body:**

```json
➡️ <REQUEST_JSON_HERE>
```

**Response Example:**

```json
➡️ <RESPONSE_JSON_HERE>
```

---

## State Requirements

➡️ Describe what needs to be stored globally for this feature (or ask AI for suggest):

`<Example: list of messages, current family info, loading state>`

---

## UI Behavior

➡️ Describe what the screen should do:

`<Example: User can type a message, press send, see messages appear in a list>`

---

## Code Generation Checklist

Generate code for these files inside this feature only:

- `types.ts`
- `api/<feature>.api.ts`
- `store/<feature>.store.ts`
- `hooks/use<Feature>.ts`
- `screens/<ScreenName>.tsx`
- Any small feature-specific components (if needed)

Do NOT generate navigation or shared components unless asked.

### Addional requirement: 
➡️ Write your requirement here (No by default)
```
Example:
- UI must follow image
- ...
```

