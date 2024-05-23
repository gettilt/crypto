<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(f"# {config['name'].title()}")
]]]-->
# Crypto
<!--//[[[end]]]-->

## Mission

Tilt's mission is to map every theme to a basket of stocks for anyone to invest in. Mappings are AI generated and expert curated.
Expert improvements are accepted if they provide a better representation of a given theme.

## Theme Prompt
<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(config['prompt'])
]]]-->
A new bill, Financial Innovation and Technology for the 21st Century Act, is about to be passed ushering in a wave of innovation in financial technology that has been held back by regulation. Any company engaged in cryptocurrencies wins.
<!--[[[end]]]-->

## Theme Stocks

<!--[[[cog
import cog
import csv
import json

with open('context.json') as file:
  contexts = json.load(file)

def _get_context_str_for_ticker(ticker):
  try:
    context = contexts[ticker]
    context_str = context['chat_gpt'] or context['claude'] or ""
  except KeyError:
    context_str = ""

  return context_str

cog.outl("| Ticker  | Context | Source |")
cog.outl("| ------- | ---- | ---- |")

with open('theme.csv') as file:
  reader = csv.reader(file)
  next(reader) # skip the header
  for row in reader:
    context_str = _get_context_str_for_ticker(row[0])
    cog.outl(f"| {row[0]} | {context_str} | {row[1]} |")
]]]-->
| Ticker  | Context | Source |
| ------- | ---- | ---- |
| AMD | Advanced Micro Devices also produces GPUs used in cryptocurrency mining, positioning it to benefit indirectly. | chat_gpt,google,claude |
| COIN | Coinbase is a leading cryptocurrency exchange platform that will benefit directly from increased adoption and regulatory clarity. | chat_gpt,twitter,google,claude |
| MA | Mastercard is also integrating cryptocurrency solutions, making it a beneficiary of the fintech innovation wave. | chat_gpt |
| MARA | Marathon Digital Holdings is another significant Bitcoin mining company that stands to gain from the new regulatory landscape. | chat_gpt,twitter,google,claude |
| MSTR | MicroStrategy has significant Bitcoin holdings and will benefit from increased cryptocurrency adoption and regulatory clarity. | chat_gpt,twitter,google,claude |
| NVDA | NVIDIA produces GPUs used in cryptocurrency mining, indirectly benefiting from increased demand for mining hardware. | chat_gpt,google,claude |
| PYPL | PayPal has integrated cryptocurrency services, allowing users to buy, sell, and hold cryptocurrencies, making it a direct beneficiary. | chat_gpt,google,claude |
| RIOT | Riot Blockchain is a major player in Bitcoin mining, which will benefit from a more favorable regulatory environment. | chat_gpt,twitter,claude |
| SQ | Block Inc. (formerly Square) offers cryptocurrency trading through its Cash App, positioning it to gain from the fintech innovation wave. | chat_gpt,google,claude |
| TSLA | Tesla has invested in Bitcoin and accepts it as payment, positioning it to benefit from increased cryptocurrency adoption. | chat_gpt,claude |
| V | Visa has been exploring cryptocurrency payment solutions, positioning it to benefit from increased adoption and regulatory clarity. | chat_gpt |
| IREN |  | twitter |
| WULF |  | twitter |
| CME | CME Group operates a derivatives exchange that offers Bitcoin futures contracts. Increased trading activity in cryptocurrencies could boost demand for these financial instruments. | google,claude |
| IBKR | Interactive Brokers has introduced cryptocurrency trading functionality, allowing its clients to trade Bitcoin futures and other digital assets. | google,claude |
| SHOP |  | google |
| BTBT | Bit Digital is a Bitcoin mining company that has rapidly expanded its operations, positioning itself to benefit from increased cryptocurrency adoption. | claude |
| HIVE | HIVE Blockchain Technologies operates cryptocurrency mining facilities in Canada, Sweden, and Iceland, providing exposure to the mining segment of the industry. | claude |
| ICE | Intercontinental Exchange, the parent company of the New York Stock Exchange, has launched a digital asset platform called Bakkt, which facilitates cryptocurrency trading and custody. | claude |
| NDAQ | Nasdaq has shown interest in the cryptocurrency space, providing market surveillance technology to crypto exchanges and considering launching its own digital asset exchange. | claude |
| HOOD |  | manual |
| SCHW |  | manual |
<!--[[[end]]]-->

## License

<p>
This project is licensed under <a href="./LICENSE">AGPLv3</a>.
</p>


## Contributors

Thank you for your improvements! We appreciate all the contributions from the community.

<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  repo = config['github_repo'].lower()
  cog.outl(f'<a href="https://github.com/gettilt/{repo}/graphs/contributors">')
  cog.outl(f'  <img src="https://contrib.rocks/image?repo=gettilt/{repo}" />')
  cog.outl('</a>')
]]]-->
<a href="https://github.com/gettilt/crypto/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=gettilt/crypto" />
</a>
<!--[[[end]]]-->

## Join Our Community

<a href="https://discord.gg/4vYMhRpaMY" target="_blank">
<img src="https://discord.com/api/guilds/1179775688421683220/widget.png?style=banner3" alt="">
</a>
