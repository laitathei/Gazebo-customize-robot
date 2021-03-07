# Gazebo-customize-robot

## Create customize robot using urdf files and camera plugin function

### Files included

#### world (store the customize urdf world files)
#### rviz (store the setting that you have make in rviz)
#### launch (store the launch files for world, robot model and rviz)
#### urdf (store the customize robot description urdf files)

### Basic explanation for robot.urdf

```XML
<?xnl version="1.0" ?>
<robot name = "my_robot" xmlns:xacro="http://www.ros.org/wiki/xacro">
```
#### specifies the xnl version and the robot name

```XML
<link>
  ....
</link>
```
#### The description for the component have to declare inside link tap

```XML
<visual>
			<geometry>
				<box size ...>
			</geometry>
</visual>
```
#### The description for the component will show in Gazebo environment or rviz after declared inside visual tap
#### The geometry tap use to define the shape of the component. For example, box and cylinder

```XML
<joint>
  <origin rpy...  xyz...>
  <parent link...>
  <child link...>
</joint>
```
#### Joint tap able to link two component together
#### Origin rpy and xyz responsible for define connection position
#### Parent link is the chassis or main body
#### Child link is the extended part from main body

### Result


