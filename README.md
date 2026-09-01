# LightHeart

HTML rendering engine

## Introduction

LightHeart is a fork of KHTML designed for windows (SUBJECT TO CHANGE), based on the KParts technology and using KJS for JavaScript support.


## Usage

If you are using CMake, you need to have

    find_package(KF5KHtml NO_MODULE)

(or similar) in your CMakeLists.txt file, and you need to link to KF5::KHtml.

To use KHTML in your application, create an instance of KHTMLPart, embed it in
your application like any other KPart, and call methods to control what it
displays:

    QUrl url("https://www.kde.org");
    KHTMLPart *w = new KHTMLPart();
    w->openUrl(url);
    w->view()->resize(500, 400);
    w->show();



