# React Drawer Component

> [!NOTE]  
> Shadcn created a drawer component that is significantly better... just use that XD.

A headless, small and simple drawer component for react

## Installation

```bash
#with npm
npm install react-headless-drawer

#with pnpm
pnpm add react-headless-drawer

#with yarn
yarn add react-headless-drawer
```

## Example Usage

```tsx
import { Drawer, useDrawer } from "react-headless-drawer";
import { GripHorizontal } from "lucide-react";

const App = () => {
  const drawer = useDrawer({
    position: "bottom",
  });

  return (
    <main
      ref={drawer.containerRef}
      className="overflow-hidden h-[100dvh] relative bg-zinc-800"
    >
      <article className="flex flex-col gap-8 p-8 pb-20 h-[100dvh]">
        <h1 className="text-zinc-100 text-5xl text-center font-black">
          React Drawer Component
        </h1>
      </article>
      <Drawer.Provider {...drawer}>
        <Drawer.Root className="absolute bottom-0 left-0 w-full bg-zinc-800">
          <Drawer.Handle className="absolute bottom-full left-0 w-full flex justify-center bg-zinc-900 border-b-2 border-zinc-800 p-4">
            <GripHorizontal className="text-zinc-100" />
          </Drawer.Handle>
          <Drawer.Content className="bg-zinc-900 p-8">
            <h1>Drawer Content</h1>
          </Drawer.Content>
        </Drawer.Root>
      </Drawer.Provider>
    </main>
  );
};
```
