5.
Type Inference means that TypeScript automatically understand the type of variable or expression. Even without declaring the type separately.

 It is helpful because it reduces the need for explicit type annotations, making code cleaner and easier to read.

7.
// UNION TYPES
type ChickenBiriyani = {
  meat: "chicken";
  spiceLevel: number;
}

type BeafBiriyani = {
  meat: "beaf";
  tenderness: number;
}

type Biriyani = ChickenBiriyani | BeafBiriyani;

const myLunch: Biriyani = {
  meat: "chicken",
  spiceLevel: 7,
};

const yourDinner: Biriyani = {
  meat: "beef",
  tenderness: 9,
};

// INTERSECTION TYPE
type BiriyaniBase = {
  riceType: string;
  meatType: string;
}

type FestiveDish = {
  serveDuring: string;
  isSpecial: boolean;
}

type FestiveBiriyani = BiriyaniBase & FestiveDish

const eidSpecial: FestiveBiriyani = {
  riceType: "basmati",
  meatType: "beaf",
  servedDuring: "Eid",
  isSpecial: true,
};
