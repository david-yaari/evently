
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
npx shadcn-ui@latest add sheet
npx shadcn-ui@latest add separator

```

### Add uploadthing

Reference web site: <https://uploadthing.com/>

```bash
npm install uploadthing @uploadthing/react 
```

### Add authentication (Clerk)

Reference web site: <https://clerk.com/>

- Go to the web site
- Click on "Add Application"
- Configure the SigIn screen i.e. the \<SignIn \/\> component
- Copy the API keys to the .env.local file
- Click on "Continue in docs"

```bash
npm install @clerk/nextjs
```

- Wrap your app in \<ClerkProvider\> as indicated in the documentation
- Create a middleware.ts file, copy the content from the documentation
- Update the middleware.ts by specifing the publicRoutes and ignoredRoutes
- On the configuration screen go to the Configure sections and select User & Authentication
- on Social Connections: select the desired providers
- om Email. Phone, Username screen select Username
- on the application create a sign-in and [[...sign-in]] directory below (auth)
- create a page.tsx and just add the \<SignIn /> component
- do the same for the sign-up
- add the following in the .env.local

- NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
- NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
- NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
- NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/

- create a specific layout.tsx in the (auth)
- configure the layout by defining a Layout constant

### <https://clerk.com/docs/users/sync-data#sync-clerk-data-to-your-backend-with-webhooks>

- <https://clerk.com/docs/users/sync-data#understanding-the-webhook-payload>

```bash
npm install svix
```

- <https://clerk.com/docs/users/sync-data#create-the-endpoint-in-your-application>
- <https://clerk.com/docs/users/sync-data#add-your-signing-secret-to-your-env-local-file>

- On the Clerk dashboard go to Webhooks, add an Endopint
- Endpoint URL: x

## uery-string

```bash
npm install query-string
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

### Create a Header & Footer

- in the componets folder add a "sgared" folder
- create a Header.tsx and Footer.tsx
- update the layout.tsx in the (root) directory accordingley
- In the header add the SignedIn and SignedOut
- Add the relevant buttons (check UserButton from Clerk)

### Create a Navbar

- in the shared directory create a Navbar component (NavItems and MobileNav in this case)
- add this component to the Header component
- In the MobileNav add the Sheet components <https://ui.shadcn.com/docs/components/sheet>
- In the NavItems use a array defined in the constant directory, index.tsx for the menu items

## MongoDb Database

- In the lib directory create a mongodb, database directories and finally an index.ts
- Run the following packages

```bash
npm install mongoose mongodb
```
