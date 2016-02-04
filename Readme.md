# Strider Docker Slave

This repo describes the base docker image for running strider jobs.

To test the slave,

```bash
./slave.js < lots.json
```

And look at the great output.

# Basing images off of this

If you want to add more packages, etc. here's how to do it:

```
# My java dockerfile
FROM strider/strider-docker-slave

USER root # so we have permission to install things
RUN apt-get install -y build-essential default-jre-headless
USER strider # set the user back to strider at the end
```

## Issue Reporting

If you have found a bug or if you have a feature request, please report them at this repository issues section. Please do not report security vulnerabilities on the public GitHub issue tracker. The [Responsible Disclosure Program](https://auth0.com/whitehat) details the procedure for disclosing security issues.

## Author

[Auth0](auth0.com)

## License

This project is licensed under the MIT license. See the [LICENSE](LICENSE) file for more info.
