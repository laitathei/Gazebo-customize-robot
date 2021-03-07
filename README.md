# Gazebo-customize-robot

## Create customize robot using urdf files and camera plugin function

### Files included

* #### world (store the customize urdf world files)
* #### rviz (store the setting that you have make in rviz)
* #### launch (store the launch files for world, robot model and rviz)
* #### urdf (store the customize robot description urdf files)

### Basic explanation for robot.urdf

```XML
<?xnl version="1.0" ?>
<robot name = "my_robot" xmlns:xacro="http://www.ros.org/wiki/xacro">
```
#### Specifies the xnl version and the robot name

```XML
<link>
  ....
</link>
```
#### The description for the component have to declare inside `<link>`

```XML
<visual>
			<geometry>
				<box size ...>
			</geometry>
</visual>
```
1. #### The description for the component will show in Gazebo environment or rviz after declared inside `<visual>`
1. #### The `<geometry>` use to define the shape of the component. For example, box and cylinder

```XML
<joint>
  <origin rpy...  xyz...>
  <parent link...>
  <child link...>
</joint>
```
1. #### `<Joint>` able to link two component together
1. #### `<Origin>` rpy and xyz responsible for define connection position
1. #### `<Parent link>` is the chassis or main body
1. #### `<Child link>` is the extended part from main body

### Result


