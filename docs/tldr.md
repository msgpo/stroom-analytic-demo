# Tl;Dr
People learn in different ways.  If you like to start by seeing things working, the following steps are suggested
(assumes some familiarity with Stroom):
1. Use docker to install [Stroom v7](https://github.com/gchq/stroom/releases/latest)
1. Add the line `127.0.0.1        kafka` to `etc/hosts` file.
1. Create a python virtual environment and switch into it.
1. Configure your virtual environment to use Python 3.7.
1. Use `pip` to install `numpy` and `pandas` in your virtual environment.
1. Install [Apache Spark 2.4.3](https://archive.apache.org/dist/spark/spark-2.4.3/spark-2.4.3-bin-hadoop2.7.tgz)
1. Ensure that `$SPARK_HOME` is set to the Spark v2.4.3 installation directory and `$PATH` includes `$SPARK_HOME/bin`
1. Load content pack `demonstrator/stroom/StroomConfig-all.zip` from `demonstrator/stroom` via Stroom UI
1. Open a terminal using your virtual environment; select a Java 1.8 jdk (e.g. by using [sdkman](https://sdkman.io/) ; cd into `demonstrator/bash` and run `./startDetectUnexpectedAuthFailures.sh`
1. Open another terminal; cd into `demonstrator/bash` and run `./sendAlertsToStroom.sh`
1. Open yet another terminal; cd into `demonstrator/analytics/data/eventgen` and run command `../../../bash/sendToStroom.sh`
1. Wait for Stroom to complete its processing
1. Open dashboard “Sample Detections” to see analytic output