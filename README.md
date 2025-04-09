# Nuxt Js and shadcdn-vue
On `assets/css/main.css`, these colors are from Material UI Design specifically from here [Vuetify alert component](https://vuetifyjs.com/en/components/alerts/), since I'm stuck what color to use for primary color such green, red, etc.
```css
:root {
    ...

    /*  */
    --color-success: #4caf50;
    --color-info: #2196f3;
    --color-warning: #fb8c00;
    --color-error: #b00020;

    --color-success-tonal: #e8f5e9;
    --color-info-tonal: #e3f1fd;
    --color-warning-tonal: #fef0df;
    --color-error-tonal: #f5dfe3;
}
```

## Others
- Icons: [Lucide](https://lucide.dev/)
- CSS: [Tailwind](https://tailwindcss.com/)
- Nuxt Js: [Nuxt documentation](https://nuxt.com/docs/getting-started/introduction)
- shadcn-vue: [shadcn-vue](https://www.shadcn-vue.com/)

## Setup

Make sure to install dependencies:

```bash
pnpm install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
pnpm dev
```

## Production

Build the application for production:

```bash
pnpm build
```

Locally preview production build:

```bash
pnpm preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
