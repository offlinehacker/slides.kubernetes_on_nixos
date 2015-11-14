FROM nixos/nix:1.10
RUN nix-channel --add http://nixos.org/releases/nixpkgs/nixpkgs-16.03pre71923.3087ef3/ dev
RUN nix-channel --update
RUN nix-env -iA dev.nginx
ADD nginx.conf nginx.conf
CMD nginx -c $PWD/nginx.conf -g 'daemon off;'
