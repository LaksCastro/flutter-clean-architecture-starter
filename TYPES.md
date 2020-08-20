- ### User Resource
- Interface
```ts
interface User {
  id: number;
  name: string;
  account: string;
  text: string;
  url: string;
  share_url: string;
  profile_image_url: string;
  is_followed: boolean;
  is_banned: boolean;
  followed_count: number;
  follower_count: number;
  is_verified: boolean;
}
```

- Example
```ts
const user : User = {
  id: 453197;
  name: "にわしか";
  account: "";
  text: "おおきくなったらゔれいんずとけっこんするんだ";
  url: "https://www.pixiv.net/users/31989750";
  share_url: "https://dotpict.net/users/453197";
  profile_image_url: "https://img.dotpicko.net/523512246c9e0354cefa1acdecd14157d261af1d73231eb532b398040e815cbd.png";
  is_followed: false;
  is_banned: false;
  followed_count: 0;
  follower_count: 0;
  is_verified: true;
}
```

### Color Code Resource
- Interface
```ts
interface ColorCode {
  red: number;
  green: number;
  blue: number;
  alpha: number;
}
```

- Example
```ts
const colorCode : ColorCode {
  red: 209;
  green: 133;
  blue: 196;
  alpha: 255;
}
```
