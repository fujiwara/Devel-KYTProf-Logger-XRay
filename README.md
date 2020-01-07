# NAME

Devel::KYTProf::Logger::XRay - Logger for AWS::XRay

# SYNOPSIS

    use Devel::KYTProf::Logger::XRay;
    my $logger = Devel::KYTProf::Logger::XRay->new;
    Devel::KYTProf->logger($logger);

# DESCRIPTION

Devel::KYTProf::Logger::XRay is a logger for AWS::XRay.

See also [AWS::XRay](https://metacpan.org/pod/AWS%3A%3AXRay).

# CONFIGURATION

## segment\_name\_builder

Code ref to generate custom segment name.

Passed `%args` that from `log` method taken.

    Devel::KYTProf::Logger::XRay->new(segment_name_builder => sub {
        my (%args) = @_;
        return 'seg:' . $args{module};
    });

# LICENSE

Copyright (C) FUJIWARA Shunichiro.

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# AUTHOR

FUJIWARA Shunichiro <fujiwara.shunichiro@gmail.com>
