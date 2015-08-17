# Contributor: Mateusz Krasowski <matkras@gmail.com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-date-iso8601'
pkgver='0.004'
pkgrel='1'
pkgdesc="the three ISO 8601 numerical calendars"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl>=5.006')
makedepends=()
url='http://search.cpan.org/dist/Date-ISO8601'
source=('http://search.cpan.org/CPAN/authors/id/Z/ZE/ZEFRAM/Date-ISO8601-0.004.tar.gz')
md5sums=('e8efa8355310f95605f8f7f399ecb5e0')
sha512sums=('41acf14cfd93fcd067711f2120d74f2f0dc21a9279acbbcaff349d3819f4d96fdb30ad688f950563875486dec791da2924c8d5a33e849c82e0b399d8375f6533')
_distdir="Date-ISO8601-0.004"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install
  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
