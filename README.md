
# evently project

## Quick Start

### Create the application

```bash
npx create-next-app@latest ./
```

### Add shadcn

Reference web site: <https://ui.shadcn.com/>

```bash
npx shadcn-ui@latest init
```

accept the default values but specify the tailwind.config.ts file (instead of js)

#### Add the following ui components

```bash
npx shadcn-ui@latest add button
```

### Add uploadthing

Reference web site: <https://uploadthing.com/>

```bash
npm install uploadthing @uploadthing/react 
```

## Configuring the application

Add route groop (root) and (auth) too keep the folder and structure clean.

### Configure the layout.tsx

- import the Poppins font
- update the metadata
- update the className

### Import the public folder

- add icons and images
- update the favicon.ico (to be placed on the app directory)

### Configure spefic layout.tsx

- add a layout.tsx in the (root) directory
- copy only the export default function RootLayout section
- remove the className as it is not needed (already provied by the global layout.tsx)
