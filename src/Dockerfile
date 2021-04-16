FROM vimagick/dsvpn@sha256:2b0b3144f17f7abbffa32a86a1ae624ab22c859eb5b9925edd14a1aa29028b59
COPY bin/ /usr/local/bin/
ENTRYPOINT ["/usr/local/bin/entrypoint"]
CMD ["server", "vpn.key", "auto", "443"]
