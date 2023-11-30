# Tebex Headless API Wrapper

![Tebex Headless](https://cdn.discordapp.com/attachments/819864517680562198/1179556907975974952/tebex.png?ex=657a36f9&is=6567c1f9&hm=6d8af61b0fadf03cb0acfe2b086667f66fca0eecf0608cac570dd1cdb9ba03ea&)

Welcome to the Tebex Headless API Wrapper! This Node.js TypeScript library allows you to seamlessly integrate Tebex into your projects and build a custom storefront without revealing your use of Tebex.

## Installation

```bash
npm install tebex_headless
```

## Getting Started

1. Obtain your Tebex Headless API public token from your Tebex account.
2. Install the `tebex_headless` library in your project.
3. Start using the Tebex Headless API in your Node.js TypeScript application!

```typescript
import { SetWebstoreIdentifier } from "tebex_headless";

SetWebstoreIdentifier("your_public_token")
```

## Functions

```typescript
// Get all categories of the webstore
async GetCategories(includePackages?: boolean, basketIdent?: string, ipAddress?: string)

// Get a specific category by an id
async GetCategory(id: number, includePackages?: boolean, basketIdent?: string, ipAddress?: string)

// Apply a coupon, gift card, or creator code
async Apply<T>(t: T, basketIdent: string, type: ApplyType)

// Remove a coupon, gift card, or creator code
async Remove<T>(t: T, basketIdent: string, type: ApplyType)

// Get a specific package by an id inside a basket
async GetPackage(id: number, basketIdent?: string, ipAddress?: string)

// Get all packages of the webstore inside a basket
async GetPackages(basketIdent?: string, ipAddress?: string)

// Get a basket by an identifier
async GetBasket(basketIdent: string)

// Create a basket and provide complete and cancel URLs
async CreateBasket(urls: Urls)

// Get all auth URLs by a basket
async GetBasketAuthUrl(basketIdent: string, returnUrl: string)

// Add a package to a specific basket
async AddPackageToBasket(basketIdent: string, package_id: number, quantity: number, type: PackageType)

// Gift a package to a target user
async GiftPackage(basketIdent: string, package_id: number, target_username_id: string)

// Remove a package inside a specific basket and package_id
async RemovePackage(basketIdent: string, package_id: number)

// Update the quantity of a package inside a basket
async UpdateQuantity(basketIdent: string, package_id: number, quantity: number)

// Get webstore information by the public token
async GetWebstore()
```

## Features

- **Seamless Integration:** Use Tebex functionalities in your project without exposing the fact that you are using Tebex.
- **Custom Storefront:** Build your custom storefront by leveraging Tebex Headless API.

## Contributing

We welcome contributions from the community! If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and ensure tests pass.
4. Submit a pull request with a clear description of your changes.

## Documentation

Check out the [official Tebex documentation](https://docs.tebex.io/) for detailed information about the Tebex Headless API and its features.

## Support

If you have questions or need assistance, feel free to [open an issue](https://github.com/grp-gg/tebex_headless/issues) on the GitHub repository.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Happy coding! 🚀