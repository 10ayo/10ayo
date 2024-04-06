import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.layout.Pane;
import javafx.scene.shape.Polygon;
import javafx.stage.Stage;

public class TriangleJavaFX extends Application {

    @Override
    public void start(Stage primaryStage) {
        // Créer un polygone pour représenter le triangle
        Polygon triangle = new Polygon();
        
        // Ajouter les points du triangle
        triangle.getPoints().addAll(100.0, 100.0, 200.0, 50.0, 300.0, 100.0);
        
        // Créer un conteneur pour le triangle
        Pane root = new Pane();
        root.getChildren().add(triangle);
        
        // Créer la scène et afficher le triangle
        Scene scene = new Scene(root, 400, 200);
        primaryStage.setScene(scene);
        primaryStage.setTitle("Triangle en JavaFX");
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
