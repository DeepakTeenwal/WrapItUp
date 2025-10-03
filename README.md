# 🎈 WrapItUp - Farcaster Mini App

A beautiful NFT minting mini app built for Farcaster that allows users to claim unique NFTs on Base network.

## 🌟 Features

- **🎨 Beautiful UI**: Stunning gradient design with floating animated shapes
- **🔗 Wallet Integration**: Seamless wallet connection using Farcaster Mini App connector
- **🎲 Random NFT Display**: Rotates between 4 unique NFT images on each app load
- **⛓️ Base Network**: Deploys and mints NFTs on Base blockchain
- **✅ Claim Protection**: Prevents duplicate claims with smart contract validation
- **📱 Responsive Design**: Optimized for mobile and desktop Farcaster clients
- **🔔 Transaction Tracking**: Direct links to BaseScan for transaction verification

## 🖼️ NFT Artwork

**NFT Images Credit:** [@alessandromalossi](https://instagram.com/alessandromalossi) on Instagram

All NFT artwork used in this project is credited to the talented artist Alessandro Malossi. Please visit their Instagram for more amazing work!

## 🚀 Getting Started

### Prerequisites

- Node.js 22.11.0 or higher
- A Farcaster account with Developer Mode enabled
- NFT contract deployed on Base network

### Installation

1. **Clone the repository**
```bash
git clone <your-repo-url>
cd wrapitup
```

2. **Upload NFT Images**
   
   Place your 4 NFT images in the public folder:
   - `0.png`
   - `1.png`
   - `2.png`
   - `3.png`
   - `image.png` (for meta tag preview)
   - `splash.png` (for splash screen)

3. **Update Contract Address**
   
   In `index.html`, update the contract address:
   ```javascript
   const CONTRACT_ADDRESS = '0xYourContractAddressHere';
   ```

4. **Deploy to Vercel**
```bash
vercel deploy
```

### Enable Farcaster Developer Mode

1. Log in to Farcaster (mobile or desktop)
2. Visit: [https://farcaster.xyz/~/settings/developer-tools](https://farcaster.xyz/~/settings/developer-tools)
3. Toggle on "Developer Mode"

## 📦 Project Structure

```
wrapitup/
├── index.html              # Main mini app file
├── public/
│   ├── 0.png              # NFT Image 1
│   ├── 1.png              # NFT Image 2
│   ├── 2.png              # NFT Image 3
│   ├── 3.png              # NFT Image 4
│   ├── image.png          # Preview image
│   └── splash.png         # Splash screen image
├── .well-known/
│   └── farcaster.json     # Mini app manifest
└── README.md
```

## 🔧 Configuration

### Mini App Manifest

Create a .well-known/farcaster.json file

### Smart Contract

The mini app interacts with an ERC-721 NFT contract on Base with the following key functions:

- `claimNFTs()`: Mint 4 NFTs to the caller
- `hasClaimed(address)`: Check if an address has already claimed
- `balanceOf(address)`: Get NFT balance of an address

## 🎯 How It Works

1. **User Opens App**: A random NFT image from the 4 available is displayed
2. **Connect Wallet**: User connects their Farcaster wallet
3. **Claim Check**: App verifies if user has already claimed NFTs
4. **Mint NFTs**: User can mint their NFTs if they haven't claimed yet
5. **Transaction Complete**: User receives confirmation with BaseScan link

## 🛠️ Technologies Used

- **Farcaster Mini App SDK**: For Farcaster integration
- **Wagmi Core**: Ethereum wallet interactions
- **@farcaster/miniapp-wagmi-connector**: Farcaster wallet connector
- **Base Network**: L2 blockchain for NFT deployment
- **HTML/CSS/JavaScript**: Core web technologies

## 📝 Smart Contract Details

- **Network**: Base
- **Contract Address**: `0xYou`
- **Standard**: ERC-721
- **Supply**: Unlimited
- **Price**: Free (gas fees only)
- **Claim Limit**: 4 NFTs per wallet (one-time claim)

## 🎨 UI/UX Features

- Gradient purple background with floating animated shapes
- Glassmorphism card design
- Smooth hover effects and transitions
- Responsive layout for all screen sizes
- Toast notifications for user feedback
- Loading spinners for async operations
- Pulse animations for connection status

## 🔐 Security Features

- One-time claim per wallet address
- Smart contract validation
- Transaction preview in wallet
- Direct BaseScan verification links

## 📱 Testing

1. Open your deployed URL in a Farcaster client
2. Test wallet connection
3. Verify claim status check
4. Test minting flow
5. Verify transaction on BaseScan

## 🐛 Troubleshooting

### App doesn't load
- Ensure Developer Mode is enabled in Farcaster
- Check console for errors
- Verify all image URLs are accessible

### Wallet won't connect
- Confirm you're using a Farcaster client
- Check that Base network is supported
- Verify Wagmi connector is properly configured

### Minting fails
- Ensure contract is deployed on Base
- Check if user has already claimed
- Verify contract ABI matches deployed contract

## 📚 Resources

- [Farcaster Mini Apps Documentation](https://docs.farcaster.xyz/)
- [Wagmi Documentation](https://wagmi.sh)
- [Base Network](https://base.org)
- [Alessandro Malossi on Instagram](https://instagram.com/alessandromalossi)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **NFT Artwork**: [@alessandromalossi](https://instagram.com/alessandromalossi) - Thank you for the amazing artwork!
- **Farcaster Team**: For the excellent Mini Apps platform
- **Base Network**: For providing a fast and affordable L2 solution
- **Wagmi Team**: For the powerful Ethereum libraries

## 📧 Contact

For questions or support, please open an issue in the repository.

---

Made with 💜 for the Farcaster community
