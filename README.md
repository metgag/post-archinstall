## paru
`git clone https://aur.archlinux.org/paru.git`

## yazi
https://yazi-rs.github.io/

### dep
`sudo pacman -S yazi ffmpeg 7zip jq poppler fd ripgrep fzf zoxide imagemagick
paru -S resvg`

### shell wrapper
`function y() {
	local tmp="$(mktemp -t "yazi-cwd.XXXXXX")" cwd
	yazi "$@" --cwd-file="$tmp"
	IFS= read -r -d '' cwd < "$tmp"
	[ -n "$cwd" ] && [ "$cwd" != "$PWD" ] && builtin cd -- "$cwd"
	rm -f -- "$tmp"
}`

## postgresql
`sudo pacman -S postgresql rainfrog`
- https://wiki.archlinux.org/title/PostgreSQL
- https://github.com/achristmascarl/rainfrog

## read or write usb drive using pcmanfm 
`sudo pacman -S pcmanfm gvfs gvfs-mtp gvfs-gphoto2 udisks2 polkit ntfs-3g exfatprogs dosfstools`
