# SOON Favorites dApp

A dApp built on SOON that allows users to store their favorite number, color, and hobbies on the SOON testnet.

## Project Structure

```
soon-app/
├── anchor-program/    # Program written in Anchor
├── src/               # Frontend Next.js application
├── .eslintrc.json
├── .gitignore
├── next-env.d.ts
├── next.config.mjs
├── package.json
├── pnpm-lock.yaml
├── postcss.config.mjs
├── tailwind.config.ts
└── tsconfig.json
```

## Prerequisites

- Node.js 20+ and pnpm
- Rust and Cargo
- Solana CLI tools
- Anchor CLI
- Solana Wallet (for testnet interaction)

## Anchor Program Deployment

1. Navigate to the anchor program directory:

```bash
cd anchor-program
```

2. Build the program:

```bash
anchor build
```

3. Get the program ID:

```bash
solana address -k target/deploy/favorites-keypair.json
```

4. Update the program ID in:

   - `Anchor.toml`
   - `lib.rs`
   - Frontend configuration

5. Deploy to testnet:

```bash
anchor deploy
```

## Frontend Setup

1. Install dependencies:

```bash
pnpm install
```

2. Run the development server:

```bash
pnpm dev
```

3. Build for production:

```bash
pnpm build
```

## Testing the Application

1. Connect your Solana(SOON compatible) wallet to testnet

2. Ensure you have some SOON tokens on testnet

   - You can get them from the faucet: [[Testnet Faucet Link](https://faucet.soo.network/)]

3. Navigate to http://localhost:3000

4. Input your favorites:

   - Enter a favorite number
   - Choose a favorite color
   - Add up to 5 hobbies

5. Click "Save Favorites" to store your data on-chain

6. View the transaction on the explorer:
   - Transaction link will appear after successful submission
   - Visit https://explorer.testnet.soo.network to view details

## Program Commands

Test the Anchor program:

```bash
anchor test
```

Build the program:

```bash
anchor build
```

Deploy to testnet:

```bash
anchor deploy
```

## Frontend Commands

Development server:

```bash
pnpm dev
```

Build the application:

```bash
pnpm build
```

Start production server:

```bash
pnpm start
```

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request
