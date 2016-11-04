# MoniScope Specifications

## Graphical Design and UX

### Slide 1 - Home page, login screen

Not much to talk about here. Industry standard login options. The arrow at the bottom indicates that there is more on the web page. That's where the description of the service, contact info and other usual home page stuff is going to be.


### Slide 2, Slide 3 - Main view

#### Stage 1 Functionality

Basically a Google Maps style, most of the view is a map showing instruments. The navigation of the map should work in the same way as it works in Google Maps.

By default, an instrument is presented as a single point. The shape and the color of the point indicates the sensor type. If there is enough room for a label with the last measurement, the label is going to show up beside the point (see Slide 2 as an example). If the instrument takes more than one measurement, the label shows more than multiple measurements separated in some way (comma?) or it just shows a single and a default one for the given type of the instrument. The label can be changed in the **Instrument Settings** to show other measurement(s).

Both the color and the shape of the point can be changed in **Instrument Settings**. If alert levels are set for any of the measurements, the color is going to indicate the current alert (Purple - level -3, Blue - level -2, Cyan - level -1 , green - OK, yellow - level 1, orange - level 2, red - level 3).

If the sensor stops responding for any reason (in other words, the measurement was not received within a specified amount of time as set in the **Instrument Settings**), the point color is going to turn gray and the label is going to show an exclamation mark. 

Hovering over the point will bring up a box showing more information about the instrument - small time domain graph of the default measurements of the instrument, last values of the other measurements (for example instruments battery voltage), timestamps of the last measurement.

Double clicking the point will bring up the detailed time graph of the measurements (See Slide 5).

Right clicking the point will show a context menu with options like **Instrument Settings**.

The upper right input box allows searching sensors by name. If a name is typed, the sensors highlight and if necessary, the map zooms out after a second or two to show all highlighted sensors which match the name. The name match is partial and case insensitive. 

Every instrument is assigned to a layer. All new instruments are going to show up on a *Default* layer. The upper left combo box allows selecting and deselecting layers and if the user does so, the points are going to show up or disappear accordingly. If an instrument name is typed in the search box and the instrument is on a deselected layer, a warning text is going to show up below the search box indicating that.

#### Stage 2 Functionality

It will be possible to create instrument groups - right click anywhere on the map and and select **Create Group** from context menu. 
The sensors can be dragged into the group. 
If alerts are set on any sensor, the group will show the respective color. If there is more than one sensor which is in alert, the highest or lowest alert color will be shown - depending on the selected group setting. 
If any of the grouped sensors names match the search input box string, the group is highlighted to indicate that the searched point is inside.
If group is clicked, the default behavior is going to be: sensors in the group show up in star like layout around the group point and show their labels if there will be enough room for them.
For specific types of sensors (for example an inclinometer chain), clicking on a group brings up a different kind of view - a composite graph. *The slide showing that will be added later*.

### Slide 4 - Instrument settings

The instruments can be selected on the map, either by clicking them, or dragging a rectangle to select more than one instrument (CTRL+drag, since simple drag is going to be map panning). Once selected, right click will give an option to go to **Instrument Settings** and show the view as in Slide 4. 

The settings page will show settings for both single and multiple points. If multiple points are selected, then the settings page will have the following behavior:
 * The settings which set as same for all selected instruments will be shown as normal
 * The settings which differ will show *VARIES*
 * The settings which are unique for each instrument (for example name) will be grayed out and disabled