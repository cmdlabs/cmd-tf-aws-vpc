# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.12.0] - 2022-01-19
- Changed syntax in vpc-endpoints.tf (route_table_ids) to remove deprication warnings.

## [0.11.0] - 2020-10-08
- Added options `enable_db_subnet_group`, `enable_redshift_subnet_group`, `enable_elasticache_subnet_group` allowing you to disable created subnet groups. Useful when IAM/SCP permissions dont allow those services. 

## [0.10.0] - 2020-09-01
### Breaking
- upgraded required_providers format to Terraform 0.13 (compatible with Terraform >= 0.12.26)

## [0.9.1] 2020-07-09
- Added output for RDS/ElastiCache/Redshift subnet group ids

## [0.9.0] 2020-06-28
- Added RDS/ElastiCache/Redshift subnet groups

## [0.8.0] 2020-06-16
### Added
- Added tier netnum variables to allow overriding tier subnet ordering

## [0.7.2] 2020-06-15
### Added
- Fixed secure_tier_subnet_cidr output

## [0.7.1] 2020-06-10
### Added
- Added route table ids outputs for each tier.

## [0.7.0] 2020-04-24
### Breaking
- Added outputs to simplify multi module stacks. Existing outputs have been renamed to be more appropriate.

## [0.6.0] 2020-02-18
### Breaking
- `nacl_public_custom`, `nacl_private_custom` and `nacl_secure_custom` are now maps rather than lists. This resolves the issue where changing the list order required 2 terraform apply runs to complete the update. See the examples folder the map structure.

### Fixed
- Fixed NACL that denys traffic between public and secure subnets.

## [0.5.1] 2019-09-19
### Fixed
- Fix the versions required to use this module

## [0.5.0] 2019-09-19
### Added
- Allow the `protocol` option in NACL rules to use either string or number

## [0.4.1] 2019-09-18
### Fixed
- Add routing to gateway VPC endpoints from both private and secure subnets

## [0.4.0] 2019-09-18
### Added
- Add feature to enable gateway VPC endpoints

## [0.3.0] 2019-09-12
### Added
- Add feature to enable VPC endpoints

## [0.2.0] 2019-06-12
- Add `nacl_allow_all_http` and `nacl_allow_all_https` to add http/https egress rules to all NACLs

## [0.1.0] 2019-06-09
- Initial release
