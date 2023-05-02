FROM rust:buster AS lsp-build
# build lsp
RUN git clone https://github.com/monaqa/satysfi-language-server \
    && cd satysfi-language-server \
    && cargo install --path . --root /usr/local/bin

FROM amutake/satysfi AS dev-env

# add lsp
COPY --from=lsp-build /usr/local/bin/satysfi-language-server /usr/local/bin

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
