# 🌍 [中文文档](./README.md) | 🚀 TronApi3🔥🔥🔥

**TronApi3** is a carefully crafted project by a dedicated development team, designed for the hottest Tron ecosystem. We offer a complete API integration solution for Tron, helping beginners quickly get into blockchain development and easily get started!

If you're talking big to your boss or need development support, let's chat! I may be able to help you solve big problems.  
⚡ **No backdoors, no encryption**, the code is simple and easy to understand, based on **ThinkPHP**, making secondary development easy, and supports deployment as a stand-alone API for internal use.

I can help you complete Tron development quickly, avoid common pitfalls, and answer all related questions, giving your project a smooth takeoff! 🌍

🌟 **TronApi3** makes blockchain development easy! We help you avoid all the pitfalls, smooth out the development process, and make it easy to bring your project to life from scratch! 🚀

🔊 Undertaking development requests in all programming languages, including but not limited to Python, Golang, PHP, Java, etc. 💓
---

## 🌐 Important Links

- **Test Address**: [Test API](https://trx.phpcode.site/)
- **Online Documentation**: [TronApi3 Docs](https://tronapi.gitbook.io/trx)
- **Project Official Website**: [TronApi3 Official Website](https://www.phpcode.site/)

---

## 📈 Our Capabilities

If you are a **boss** 👔 and don't have a development team, no worries! We can handle all your development needs. Since **2020**, we've successfully completed multiple large-scale international projects, each with a transaction volume of over **100,000,000 USDT** 🌟.

### Key Advantages:
- **Efficient development**, no delays
- **Strong operational capability**, projects implemented in multiple countries
- **Multilingual support**, future self-operation without dependence on developers
- **Full-service, high-quality delivery**, you can fully trust us to handle everything

---

## 📦 Project Overview

**TronApi3** is a simple and easy-to-understand, feature-rich Tron blockchain API interface that supports the following core functions:
- Create wallet 🏦
- **USDT transfer** 💸
- **TRX transfer** 🔄
- Check balance 💰
- **Private key to address** 🔑➡️📍

All APIs support **GET requests**, and for higher security, you can use **POST requests**.  
This project is not only suitable for beginners to learn blockchain principles but also supports some simple development needs.

---

## 💻 Technical Architecture

**TronApi3** is developed based on the **ThinkPHP 5** framework. The code is clean and easy to understand, making it easy for you to get started and modify for secondary development or deployment as an API service.

---

## 🛠 Installation Guide

1. **PHP 7.3 or 7.4** environment
2. Install **GMP extension** (otherwise, transfers will fail)
3. Configure **URL rewriting**
4. Set the runtime directory to the `public` folder
5. No need to modify the contract address
6. After configuring, disable debug mode for security

---

## 🔑 API Key Configuration

If you need to increase the API call limits, it is recommended to apply for an **API Key** to avoid restrictions.  
[Apply for API Key](https://www.trongrid.io/)

<!-- 
下面的不会显示

### Configuration Steps:

1. Open the file `vendor/fenguoz/tron-php/src/Api.php`
2. Replace the `post` method as follows:

```php
/**
 * Handles common functionality, such as formatting POST data and error handling
 *
 * @throws TronErrorException
 */
public function post(string $endpoint, array $data = [], bool $returnAssoc = false)
{
    if (sizeof($data)) {
        $data = [
            'headers' => [
                'TRON-PRO-API-KEY' => 'your api key'  // Insert your API key here
            ],
            'json' => $data
        ];
    }
    $stream = (string)$this->getClient()->post($endpoint, $data)->getBody();
    $body = json_decode($stream, $returnAssoc);
    $this->checkForErrorResponse($returnAssoc, $body);
    return $body;
}
```

 -->

## 📞 Contact Us
For support or to purchase the source code, feel free to contact:

Telegram: 🍭🍭🍭 [@king_orz](https://t.me/king_orz)   




## Install

```bash
> composer require iexbase/tron-api --ignore-platform-reqs
```
## Requirements

The following versions of PHP are supported by this version.

* PHP 7.4

## Example Usage

```php
use IEXBase\TronAPI\Tron;

$fullNode = new \IEXBase\TronAPI\Provider\HttpProvider('https://api.trongrid.io');
$solidityNode = new \IEXBase\TronAPI\Provider\HttpProvider('https://api.trongrid.io');
$eventServer = new \IEXBase\TronAPI\Provider\HttpProvider('https://api.trongrid.io');

try {
    $tron = new \IEXBase\TronAPI\Tron($fullNode, $solidityNode, $eventServer);
} catch (\IEXBase\TronAPI\Exception\TronException $e) {
    exit($e->getMessage());
}


$this->setAddress('..');
//Balance
$tron->getBalance(null, true);

// Transfer Trx
var_dump($tron->send('to', 1.5));

//Generate Address
var_dump($tron->createAccount());

//Get Last Blocks
var_dump($tron->getLatestBlocks(2));

//Change account name (only once)
var_dump($tron->changeAccountName('address', 'NewName'));


// Contract
$tron->contract('Contract Address');



```

## Testing

``` bash
$ vendor/bin/phpunit
```
