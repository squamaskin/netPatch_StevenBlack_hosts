## NetPatch Firewall + StevenBlack hosts

Проба блокировки рекламы и треккеров для android.

Создание группы доменов для [NetPatch Firewall](https://netpatch.github.io/) из [списка StevenBlack hosts](https://github.com/StevenBlack/hosts)



## VS Code
преобразование списка "StevenBlack/hosts" через редактор VS Code (пока вручную...)

#### Шаги
- из [списка StevenBlack hosts](https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts) оставить только домены
- rm 0.0.0.0 `CTRL+H` => `0.0.0.0 ` => ``
- rm comments `CTRL+H` => `#.*` => ``
- rm empty lines `CTRL+H` => `^\s*$\n` => ``
- (!problem)prepare domains `CTRL+H` => `^(?:w{3}\.)?.*?([^.\r\n\/]+\.)([^.\r\n\/]+\.[^.\r\n\/]{2,6}(?:\.[^.\r\n\/]{2,6})?).*$` => `$2`
- rm duplicates `CTRL+A CTRL+SHIFT+P` => `Delete Duplicate Lines`
- sort `CTRL+A CTRL+SHIFT+P` => `Sort Lines Ascending`
- (!problem)add "." before domain `CTRL+H` => `(^.*)$` => `.$1`

## NetPatch Firewall
- загрузить список в группу [https://raw.githubusercontent.com/squamaskin/netPatch_StevenBlack_hosts/master/ad.txt](https://raw.githubusercontent.com/squamaskin/netPatch_StevenBlack_hosts/master/ad.txt)