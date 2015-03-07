# NAME

App::cpan::zero - cpanm or carton helper for dependencies on git repositories

# SYNOPSIS

    $ cat cpanfile
    requires 'Test::PackageName', git => 'git://github.com/shoichikaji/Test-PackageName.git@master';

    $ cpan-zero cpanm -nq -Llocal --installdeps .
    # or
    $ cpan-zero carton install

# DESCRIPTION

App::cpan::zero helps cpanm or carton when dependencies are on git repositories.

I'm looking forward to cpanm and carton's native git support!

# HOW IT WORKS

- find dependencies which are on git repositories in `cpanfile`
- inject them to local mirror and make index by [OrePAN2](https://metacpan.org/pod/OrePAN2)
- execute cpanm or carton with `--mirror local-mirror`

# SEE ALSO

[App::cpanminus](https://metacpan.org/pod/App::cpanminus)

[Carton](https://metacpan.org/pod/Carton)

[OrePAN2](https://metacpan.org/pod/OrePAN2)

[cpanfile](https://metacpan.org/pod/cpanfile)

# LICENSE

Copyright (C) Shoichi Kaji.

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# AUTHOR

Shoichi Kaji <skaji@cpan.org>
