[DarkSystemCD®](https://github.com/DarkSystemCD) \ [CSharp](https://github.com/DarkSystemCD/CSharp) \ [PROJECTS]() \ **Moving Controls**
<p align="center">
  <img src="https://i.imgur.com/e3jUBda.jpg" title="BloodArt: Computer Software" height="320" width="780">
</p>

# ⚙️ Moving Controls;
> WDS.DarkBrain(DarkSystemCD)[logic production engine]<br>

🚧version 0.1<br>
`Samples on how to structure and set feature ready from a blank application, moving controls on window;`<hr>

```c#
namespace WpfApp1
{

  /*  WDS.DarkBrain(DarkSystemCD)[logic production engine]                   */
  /// <summary>Interaction logic for App.xaml</summary>
  public partial class App : System.Windows.Application
  {

    private App()
    {
      //[?]SetApplicationProperties:MoveControls;
      Current.Properties["MoveHost"] = null;
      Current.Properties["MoveControl"] = null;
      Current.Properties["Moving"] = false;
      Current.Properties["MovePoint"] = null;

      //[?]CreateApplicationWindow;
      var v90 = new System.Windows.Window()
      {
        HorizontalContentAlignment = System.Windows.HorizontalAlignment.Left,
        VerticalContentAlignment = System.Windows.VerticalAlignment.Top,
        Margin = new System.Windows.Thickness(0,0,0,0),
        Width = 600,
        Height = 400
      };

      //[?]CreateApplication:WindowHostControl;
      var v91 = new System.Windows.Controls.Grid()
      {
        HorizontalAlignment = System.Windows.HorizontalAlignment.Stretch,
        VerticalAlignment = System.Windows.VerticalAlignment.Stretch,
        Margin = new System.Windows.Thickness(0,0,0,0)
      };

      //[?]CreateMovingControl:SampleCode;
      var v92 = new System.Windows.Controls.Label()
      {
        HorizontalAlignment = System.Windows.HorizontalAlignment.Left,
        VerticalAlignment = System.Windows.VerticalAlignment.Top,
        Background = System.Windows.Media.Brushes.DeepPink,
        Foreground = System.Windows.Media.Brushes.White,
        Content = "Move the Label"
      };
      v92.MouseDown += new System.Windows.Input.MouseButtonEventHandler(App.MouseDown);
      v92.PreviewMouseMove += new System.Windows.Input.MouseEventHandler(App.MouseMove);
      v92.MouseUp += new System.Windows.Input.MouseButtonEventHandler(App.MouseUp);

      v91.Children.Add(v92);
      v90.Content = v91;
      v90.Show();
    }

    internal static void MouseDown(System.Object sender,System.Windows.Input.MouseButtonEventArgs e)
    {
      var v90 = (System.Windows.FrameworkElement)sender;
      //[?]SetControl;
      App.Current.Properties["MoveControl"] = v90;
      //[?]SetCoordinates;
      App.Current.Properties["MovePoint"] = e.GetPosition(v90);
      //[?]LockCursorToControl;
      System.Windows.Input.Mouse.Capture(v90);
      //[?]SetMovementIndicator;
      App.Current.Properties["Moving"] = true;
    }

    internal static void MouseMove(System.Object sender,System.Windows.Input.MouseEventArgs e)
    {
      //[?]CheckMovementIndicator;
      if(((System.Boolean)App.Current.Properties["Moving"]) == true)
      {
        var v90 = (System.Windows.FrameworkElement)App.Current.Properties["MoveControl"];
        //[?]GetHostCoordinate;
        var currentPoint = e.GetPosition(
          ((System.Windows.FrameworkElement)App.Current.Properties["MoveHost"])
          );
        //[?]CheckMouseButton;
        if(e.LeftButton == System.Windows.Input.MouseButtonState.Pressed)
        {
          //[?]UpdateControlPosition;
          v90.Margin = new System.Windows.Thickness(
                currentPoint.X - ((System.Windows.Point)App.Current.Properties["MovePoint"]).X,
                currentPoint.Y - ((System.Windows.Point)App.Current.Properties["MovePoint"]).Y,
                v90.Margin.Right,v90.Margin.Bottom
                );
        }
      }
    }

    internal static void MouseUp(System.Object sender,System.Windows.Input.MouseButtonEventArgs e)
    {
      App.Current.Properties["Moving"] = false;
      App.Current.Properties["MoveControl"] = null;
      System.Windows.Input.Mouse.Capture(null);
    }

  }

}
```
<hr>

### Descriptions
* **Application Properties**<br>
 used instead of global variables to host moving control event data;
* **Horizontal** and **Vertical Alignment, Margin**<br>
used at Window and Host Container to proper indicate moving control functionally;
* **Mouse Events**<br>
used as standardize mouse operations that can be set to controls in the application;
* **(System.Windows.FrameworkElement)**<br>
 used to perform compatibility in access to common control properties of from different types for usability;
* System.Windows.Input.Mouse.Capture<br>
 used to prevent Moving Control operations from losing focus out from default situations;
* System.Windows.Thickness<br>
used as the source control for positioning coordenates of a element in the application window Host container;

`this sample setup illustrate the usability of mouse operations in the application;`<br>
`resulted of organizing code in the quality of DarkSystemCD projects;`

<hr><div align="right"><sup>thanks for choosing DarkSystemCD.</sup>

[![foo](https://github.githubassets.com/favicon.ico "DarkSystemCD®")](https://github.com/DarkSystemCD) [![foo](https://drive.google.com/uc?authuser=0&id=1vpdRLX_DSKkjvSIkBgyTMRC-2x_FOyf3 "DarkSystemCD®")](https://sites.google.com/view/darksystemcd) [![foo](https://a-v2.sndcdn.com/assets/images/sc-icons/favicon-2cadd14bdb.ico "DarkSystemCD®")](https://soundcloud.com/darksystemcd)

</div>

<!--
when society where to claim the intellectual effort from computer projects
DarkSystemCD suffered plot situations on which productivity where absent from others perceptions

a world of manipulative endeavors resulted of canvases of the moral order
faces that ghostely to possess the processes build from oceans drops of fame issues
where cicling the surrounding for brainwash activities;

importances that to compare at cultural magnitude the valuable precence at the world;
identified of a defeat for lost values of participation, here the hate in a war of smiles;
-->

###### DarkSystemCD® used to identify, meet, work and publish logics and programming design, software, games and music on interfaces and electronic, digital and virtual media.

###### BloodArt.Magazine detailed description available in the projects and productions, developing delivered to collection information in the magazine.

###### WDHellS a virtual personal person trademark and nickname, created for display my creations enabling it’s available world wide.
