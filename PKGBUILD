# Maintainer: Helder Bertoldo <helder.bertoldo@gmail.com>

pkgbase='dynamic-wallpaper-bigsur-cliffs-dragged'
pkgname=("${pkgbase}-gnome-timed-git" "${pkgbase}-kde-git" "${pkgbase}-images-git" )
_gitname='gnome-kde-dynamic-wallpaper-bigsur-cliffs-dragged'
_author=btd1337
pkgver=1.0
pkgrel=1
arch=('any')
url="https://github.com/${_author}/${_gitname}"
source=("git+https://github.com/${_author}/${_gitname}")
sha256sums=('SKIP')

pkgver() {
  cd $_gitname
  git describe --tags --long | sed -r 's/^v//;s/([^-]*-g)/r\1/;s/-/./g'
}

 package_dynamic-wallpaper-bigsur-cliffs-dragged-images-git() {
	pkgdesc="macOS bigsur-cliffs-dragged dynamic wallpaper based 8 images"
	cd "${srcdir}/${_gitname}"
	install -dm755 "${pkgdir}/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images"
	install -m644 ${srcdir}/${_gitname}/bigsur-cliffs-dragged/* "${pkgdir}/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images"
}

 package_dynamic-wallpaper-bigsur-cliffs-dragged-gnome-timed-git() {
	depends=(gnome-shell gnome-backgrounds dynamic-wallpaper-bigsur-cliffs-dragged-images-git)
	pkgdesc="Time based GNOME macOS bigsur-cliffs-dragged wallpaper with real scheludes"
	install=dynamic-wallpaper-bigsur-cliffs-dragged-gnome-timed-git.install
	cd "${srcdir}/${_gitname}"
	install -dm755 "${pkgdir}/usr/share/backgrounds/macOS"
	ln -s "/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images" "${pkgdir}/usr/share/backgrounds/macOS/bigsur-cliffs-dragged"
	install -Dm644 bigsur-cliffs-dragged-timed.xml "${pkgdir}/usr/share/backgrounds/macOS/bigsur-cliffs-dragged-timed.xml"
	install -Dm644 bigsur-cliffs-dragged.xml "${pkgdir}/usr/share/gnome-background-properties/bigsur-cliffs-dragged.xml"
 }
 
 package_dynamic-wallpaper-bigsur-cliffs-dragged-kde-git() {
	depends=('plasma5-wallpapers-dynamic>=2.3' dynamic-wallpaper-bigsur-cliffs-dragged-images-git)
	pkgdesc="Azimuth Elevation based / Time based KDE macOS bigsur-cliffs-dragged wallpaper"
	install=dynamic-wallpaper-bigsur-cliffs-dragged-kde-git.install
	cd "${srcdir}/${_gitname}"
	install -dm755 "${pkgdir}/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-timed/contents"
	ln -s "/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/contents/images" "${pkgdir}/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-timed/contents/images"
	install -Dm644 bigsur-cliffs-dragged-solar.json "${pkgdir}/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-solar/metadata.json"
	install -Dm644 bigsur-cliffs-dragged-timed.json "${pkgdir}/usr/share/dynamicwallpapers/bigsur-cliffs-dragged-timed/metadata.json"
 }
