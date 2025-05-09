## 5. Type Inference in TypeScript

**Type Inference** means that TypeScript automatically understands the type of a variable or expression, even without declaring the type explicitly.

It is helpful because it reduces the need for explicit type annotations, making the code cleaner and easier to read, while still maintaining type safety.

---

## 🔗7. Union & Intersection Types Example

```ts
type ChickenBiriyani = {
  meat: "chicken";
  spiceLevel: number;
};

type BeafBiriyani = {
  meat: "beaf";
  tenderness: number;
};

type Biriyani = ChickenBiriyani | BeafBiriyani;

const myLunch: Biriyani = {
  meat: "chicken",
  spiceLevel: 7,
};

const yourDinner: Biriyani = {
  meat: "beef",
  tenderness: 9,
};

-------------------------

type BiriyaniBase = {
  riceType: string;
  meatType: string;
};

type FestiveDish = {
  serveDuring: string;
  isSpecial: boolean;
};

type FestiveBiriyani = BiriyaniBase & FestiveDish;

const eidSpecial: FestiveBiriyani = {
  riceType: "basmati",
  meatType: "beaf",
  serveDuring: "Eid",
  isSpecial: true,
};
