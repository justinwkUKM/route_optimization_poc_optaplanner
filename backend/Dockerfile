# Copyright 2019 Red Hat, Inc. and/or its affiliates.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

FROM adoptopenjdk/openjdk8:ubi-minimal-jre
#ENV APP_ROUTING_ENGINE air
ENV APP_ROUTING_ENGINE graphhopper
ENV APP_ROUTING_OSM_DOWNLOAD_URL http://download.geofabrik.de/asia/malaysia-singapore-brunei-latest.osm.pbf
ENV APP_REGION_COUNTRY_CODES MY
ENV APP_ROUTING_OSM_FILE malaysia-singapore-brunei-latest.osm.pbf
COPY target/*-exec.jar /opt/app/tloweb-vehicle-routing.jar
WORKDIR /opt/app
VOLUME /opt/app/local
CMD ["java", "-jar", "tloweb-vehicle-routing.jar" ]
EXPOSE 8787


#FROM openjdk:8-jdk-alpine
#ENV APP_ROUTING_ENGINE graphhopper
#ENV APP_ROUTING_OSM_DOWNLOAD_URL http://download.geofabrik.de/asia/malaysia-singapore-brunei-latest.osm.pbf
#ENV APP_REGION_COUNTRY_CODES MY
#ENV APP_ROUTING_OSM_FILE malaysia-singapore-brunei-latest.osm.pbf
#COPY target/*-exec.jar /opt/app/optaweb-vehicle-routing.jar
#WORKDIR /opt/app
#VOLUME /opt/app/local
#CMD ["java", "-jar", "optaweb-vehicle-routing.jar"]
#EXPOSE 8787