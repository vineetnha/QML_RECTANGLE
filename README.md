# QML_RECTANGLE
//made a rectangle and Circle using QML
import QtQuick

Window {
    width: 640
    height: 480
    visible: true
    title: qsTr("Hello World")

    property string texttoShow: "hello"

    Row{
        anchors.centerIn: parent
        Rectangle {
            id:redrectid
            width: 100
            height: 100
            color: "red"
            radius: 35
            border.color: "black"
           // anchors.centerIn: parent

            MouseArea{
                anchors.fill: parent //
                onClicked: {
                    console.log("clicked on the red rectangle")
                   textid.text = "red"
            }
    }
        }
        Rectangle {
            id:purplerectid
            width: 100
            height: 100
            color: "purple"
            radius: 35
            border.color: "black"
//anchors.centerIn: parent

            MouseArea{
                anchors.fill: parent //
                onClicked: {
                    console.log("clicked on the purple rectangle")
                    console.log("1")
                    console.log("4")
            }
    }
        }
        Rectangle {
            id:blueRectid
            width: 100
            height: 100
            color: "blue"
            radius: 35
            border.color: "blue"
           // anchors.centerIn: parent

            MouseArea{
                anchors.fill: parent //
                onClicked: {
                    console.log("clicked on the blue rectangle")

            }
    }
        }


        Rectangle {
            id:circleid
            width: 100
            height: 100
            color: "pink"
            radius: 65
            border.color: "black"
           // anchors.centerIn: parent
            Text {
                id: textid
                anchors.centerIn: parent
                text: texttoShow
            }
            MouseArea{
                anchors.fill: parent //
                onClicked: {
                    console.log("clicked on the circle")
                    console.log("1")
                    console.log("2")
            }
    }
        }
    }



}
