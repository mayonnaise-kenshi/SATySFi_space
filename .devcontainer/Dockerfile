FROM amutake/satysfi

# ocamlのPATH通す
ENV PATH $PATH:/root/.opam/$OCAML_VERSION/bin

# tools
RUN apt update \
    && apt install -y fish

# azmath
RUN opam install satysfi-azmath && satyrographos install

#図
RUN opam install satysfi-figbox && satyrographos install

#表
RUN opam install satysfi-easytable && satyrographos install

#引用
#引用のライブラリ
RUN opam install satysfi-bibyfi && satyrographos install
#参考文献リスト生成アプリ
# RUN && git clone https://github.com/puripuri2100/BibSATySFi.git \
#     && cd BibSATySFi \
#     && opam pin add bibsatysfi . \
#     && opam install bibsatysfi
