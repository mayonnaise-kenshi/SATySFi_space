FROM amutake/satysfi

# azmath
RUN eval $(opam env) && opam install satysfi-azmath && satyrographos install

#図
RUN eval $(opam env) && opam install satysfi-figbox && satyrographos install

#表
RUN eval $(opam env) && opam install satysfi-easytable && satyrographos install

#引用
#引用のライブラリ
RUN eval $(opam env) && opam install satysfi-bibyfi && satyrographos install
#参考文献リスト生成アプリ
RUN eval $(opam env) && git clone https://github.com/puripuri2100/BibSATySFi.git \
    && cd BibSATySFi \
    && opam pin add bibsatysfi . \
    && opam install bibsatysfi

CMD eval $(opam env)