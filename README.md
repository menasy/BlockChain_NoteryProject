# Blockchain Tabanlı Noter Uygulaması

## 📋 Proje Hakkında

Blockchain teknolojisinin veri bütünlüğü, değişmezlik ve zaman damgalama özelliklerini kullanarak geliştirilmiş bir noter sistemi. Belgeler SHA256 algoritması ile hash'lenerek Ethereum Sepolia test ağına kaydedilir ve belgelerin değişip değişmediği doğrulanabilir.

## 🖼️ Proje Görselleri

### Web Arayüzü
![Web Arayüzü](https://github.com/menasy/Project_icons/blob/main/BlockChan_Web3/BlockChainNotaryWeb.png)

### Remix IDE - Deploy Edilmiş Solidity Kodu
![Remix IDE](https://github.com/menasy/Project_icons/blob/main/BlockChan_Web3/solFileRemixIDE.png)

## ✨ Özellikler

- 🔐 SHA256 hash hesaplama ile belge doğrulama
- ⛓️ Ethereum Sepolia test ağı entegrasyonu
- 🕒 Blockchain tabanlı zaman damgalama
- 🔍 Belge değişiklik kontrolü
- 🦊 MetaMask cüzdan entegrasyonu
- 🚫 Tekrarlı kayıt önleme

## 🛠️ Teknolojiler

- **Solidity** - Akıllı sözleşmeler
- **Ethereum Sepolia** - Test ağı
- **Ethers.js** - Blockchain etkileşimi
- **CryptoJS** - SHA256 hash hesaplama
- **HTML/JavaScript** - Web arayüzü
- **MetaMask** - Cüzdan entegrasyonu

## 📦 Kurulum ve Çalıştırma

### Gereksinimler
- MetaMask cüzdan eklentisi
- Sepolia test ağı ETH'si ([Faucet](https://sepoliafaucet.com/))

### 1. Projenin Hazır Hale Getirilmesi

#### Akıllı Sözleşme Deploy İşlemi:
- `notary.sol` dosyasını Remix IDE'de derleyin
- Deploy & Run bölümünde "Injected Provider" seçin
- MetaMask ile Sepolia test ağına bağlanın ve deploy edin

#### Contract Bilgilerini JavaScript'e Tanımlama:
- Deploy sonrası contract adresini alın
- JavaScript dosyasında `contractAdress` değişkenine atayın
- Contract ABI bilgisini `contractABI` değişkenine tanımlayın

#### Web Arayüzünü Başlatma:
- `index.html` dosyasını tarayıcınızda açın
- MetaMask bağlantısını onaylayın

### 2. Uygulamanın Kullanımı

#### Belge Kaydetme:
1. Web arayüzünde dosya yükleme alanından belgenizi seçin
2. "Kaydet" butonuna tıklayın
3. MetaMask'ta çıkan işlemi onaylayın
4. Blockchain'de işlem onaylanana kadar bekleyin
5. "Belge başarıyla kaydedildi" mesajını görün

#### Belge Doğrulama:
1. Doğrulama alanından aynı dosyayı yükleyin
2. Dosyanın hash'i yeniden hesaplanır
3. Blockchain'deki kayıtlı hash ile karşılaştırılır
4. Eşleşme durumunda dosyanın orijinal olduğu ve kayıt tarihi gösterilir

## 🔧 Akıllı Sözleşme

```solidity
// Belge kaydetme
function uploadDocument(bytes32 docHash) external

// Belge doğrulama
function verifyDocument(bytes32 docHash) external view returns (uint256 timestamp)
```


## 📚 Kaynaklar

- [Sepolia Etherscan](https://sepolia.etherscan.io/)
- [Blockchain Uygulama Videosu](https://www.youtube.com/watch?v=u0vhvBHd4Ro)
- [Merkle Ağacı - Investopedia](https://www.investopedia.com/terms/m/merkle-tree.asp)
- [Merkle Ağacı - Medium](https://medium.com/@rajeevprasanna/understanding-merkle-trees-the-backbone-of-data-verification-13b39af26fff)
- [Consensus Mechanism](https://www.investopedia.com/terms/c/consensus-mechanism-cryptocurrency.asp)
- [Hashing Algoritmaları](https://www.youtube.com/watch?v=2AmKrvTdH-g)
- [Solidity Temel Bilgiler](https://enginunal.medium.com/solidity-1-temel-bilgiler-40ab2ac36878)
- [Solidity Basic Syntax](https://www.geeksforgeeks.org/solidity-basic-syntax/)

## ⚠️ Not

Bu uygulama test amaçlı geliştirilmiştir ve Sepolia test ağını kullanır.